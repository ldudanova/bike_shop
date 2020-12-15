<template>
    <div>
        <div class="modal modal_md"  tabindex="-1" role="dialog" id="callbackModal">
        <div class="modal-dialog modal-dialog-centered" role="document">
            <div class="modal-content">
                <div class="modal-header">
                    <div class="modal-title h2 iconic-text">
                        <svg class="primary"  width="26" height="25" viewBox="0 0 20 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M14.7719 12.3557L17.3119 12.6457C18.3219 12.7657 19.0819 13.6157 19.0719 14.6257L18.8876 16.936C18.8876 18.066 17.9476 19.006 16.8176 18.936C15.0096 18.8236 13.2781 18.4287 11.6667 17.7948C11.3091 17.6541 10.9574 17.5017 10.6121 17.3379C7.05983 15.6532 4.18457 12.7727 2.50759 9.21438C2.34368 8.86658 2.19122 8.51231 2.05069 8.15204C1.4273 6.55388 1.03876 4.83778 0.927563 3.04597C0.857563 1.91597 1.79756 0.975974 2.92756 0.975974L5.42938 0.763184C6.44938 0.763184 7.29938 1.52318 7.41938 2.53318L7.70938 5.05318C7.77938 5.66318 7.56938 6.26318 7.13938 6.69318L4.51756 8.75597C5.95756 11.596 8.27756 13.906 11.1076 15.346L13.1319 12.9257C13.5619 12.4957 14.1619 12.2857 14.7719 12.3557ZM14.5532 14.3437L17.0652 14.6305L16.8876 16.8563V16.936C16.8876 16.9358 16.8876 16.9361 16.8876 16.936C15.5459 16.8478 14.2523 16.5835 13.0297 16.1652L14.5532 14.3437ZM5.72052 5.2647L5.43344 2.77006L3.01246 2.97597H2.92756C2.92743 2.97597 2.92769 2.97597 2.92756 2.97597C3.01608 4.32442 3.28239 5.62394 3.70394 6.8513L5.72052 5.2647Z" fill="#1A1A1A"/>
                        </svg>
                        <span class="iconic-text__text">Перезвоните мне</span>
                    </div>
                    <button type="button" class="close" data-dismiss="modal" aria-label="Close">
                        <svg width="24" height="24" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M12.946 5.8753C13.2714 5.54987 13.7991 5.54987 14.1245 5.8753C14.45 6.20074 14.45 6.72838 14.1245 7.05382L7.05345 14.1249C6.72801 14.4503 6.20037 14.4503 5.87494 14.1249C5.5495 13.7994 5.5495 13.2718 5.87494 12.9464L12.946 5.8753Z" fill="#1A1A1A"/><path d="M14.1245 12.9464C14.45 13.2718 14.45 13.7994 14.1245 14.1249C13.7991 14.4503 13.2714 14.4503 12.946 14.1249L5.87494 7.05382C5.5495 6.72838 5.5495 6.20074 5.87494 5.8753C6.20037 5.54987 6.72801 5.54987 7.05345 5.8753L14.1245 12.9464Z" fill="#1A1A1A"/></svg>
                    </button>
                </div>
                <div class="modal-body">
                    <form action="post" @submit="submitCallback">
                        <div class="row">
                            <div class="col-12 ">
                                <div class="form-group">
                                    <input id="name" type="text" required @keypress="checkInputName" class="form-control form-control_lg name" value="" placeholder="Ваше имя">
                                    <div v-if="errorsName.length" class="modal-error">
                                        <ul class="modal-error__list">
                                            <li v-for="error in errorsName" :key="error.message">{{error}}</li>
                                        </ul>
                                    </div>
                                    <input id="phone" type="tel" required @keypress="checkInputPhone" maxlength="12" class="form-control form-control_lg phone" value="" placeholder="+7___-___-__-__">
                                    <div v-if="errorsPhone.length" class="modal-error">
                                        <ul class="modal-error__list">
                                            <li v-for="error in errorsPhone" :key="error.message">{{error}}</li>
                                        </ul>
                                    </div>
                                </div>
                                <div class="form-group">
                                    <p>Нажимая на кнопку «Жду звонка!», вы даете <a href="#!" class="link link_default" target="_blank">согласие на обработку своих персональных данных</a></p>
                                </div>
                            </div>
                            <div class="col-12">
                                <button type="submit" class="btn btn_lg btn-primary btn-block">Жду звонка</button>
                            </div>
                        </div>
                    </form>

                </div>
            </div>
        </div>
    </div>
        <div class="modal-success-msg">
            <h3 class="modal-success-msg__text">
                Мы вам перезвоним!
            </h3>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'modal',
        props: {},
        data: () => ({
            errorsName: [],
            errorsPhone: [],
            name: '',
            phone: 0
        }),

        computed: {},
        methods:{

            checkInputName: function (event) {

                let char = String.fromCharCode(event.keyCode);
                if(/^[A-Za-zА-Яа-я]+$/.test(char))
                    return true;
                else
                    event.preventDefault();
            },
            checkInputPhone: function (event) {

                let keyCode = event.keyCode ? event.keyCode : event.which;
                if ( ( (keyCode < 48 || keyCode > 57) && keyCode > 31 && keyCode != 43) ) {
                    event.preventDefault();
                }

            },
            validatePhone: function () {
                let phone_input = document.querySelector('#phone').value;
                if(!/^(\+7|7|8)?[\s-]?\(?[489][0-9]{2}\)?[\s-]?[0-9]{3}[\s-]?[0-9]{2}[\s-]?[0-9]{2}$/.test(phone_input))
                {
                    this.errorsPhone.push('Неверный формат телефона.');
                }
                if(phone_input.length < 12) {
                    this.errorsPhone.push("Номер телефона слишком короткий.");
                }
            },
            validateName: function () {
                let name_input = document.querySelector('#name').value;
                if(!/^[A-Za-zА-Яа-я]+$/.test(name_input))
                {
                    this.errorsName.push('Имя может содержать только буквы');
                }
                if(name_input.length < 2) {
                    this.errorsName.push("Имя слишком короткое.");
                }
            },
            submitCallback: function (event) {
                this.errorsName = [];
                this.errorsPhone = [];
                this.validatePhone();
                this.validateName();

                if (!this.errorsName.length && !this.errorsPhone.length) {

                   return true;
                }
                event.preventDefault();
            }

        }
    }

</script>
