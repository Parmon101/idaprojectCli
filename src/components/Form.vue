<template>
    <div class="form">
        <h2>Добавление товара</h2>
        <form @submit.prevent="someAction()">
            <div class="wrap">
                <article>
                    <span>
                        <pub>Наименование товара</pub>
                        <img alt="red" src="../assets/red.svg" />
                    </span>
                </article>
                <input
                    type="text"
                    placeholder="Введите наименование товара"
                    v-model="sendName"
                    required
                />
                <div v-if="!sendName" class="errorField">Поле является обязательным</div>
            </div>

            <div class="wrap">
                <article>
                    <pub>Описание товара</pub>
                    <img alt="red" src="../assets/red.svg" />
                </article>
                <textarea name="" id="" cols="30" rows="10" placeholder="Введите описание">
                </textarea>
            </div>

            <div class="wrap">
                <article>
                    <pub>Ссылка на изображение товара</pub>
                    <img alt="red" src="../assets/red.svg" />
                </article>
                <input type="text" placeholder="Введите ссылку" v-model="sendUrl" required />
                <div v-if="!sendUrl" class="errorField">Поле является обязательным</div>
            </div>

            <div class="wrap">
                <article>
                    <pub>Цена товара</pub>
                    <img alt="red" src="../assets/red.svg" />
                </article>
                <input type="text" placeholder="Введите цену" v-model="sendPrice" required />
                <div v-if="!sendPrice" class="errorField">Поле является обязательным</div>
            </div>

            <div class="wrap">
                <button v-on:click="log" :disabled="isButtonDisabled">Добавить товар</button>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    name: 'HomeForm',
    data() {
        return {
            name: null,
            submitValid: false,

            isButtonDisabled: true,
            canSend: false,
            sendName: '',
            sendUrl: '',
            sendPrice: '',
        };
    },
    watch: {
        sendName: function () {
            this.canSend =
                this.sendName.length && this.sendUrl.length && this.sendPrice.length >= 1;
            this.isButtonDisabled = !this.canSend;
        },
        sendUrl: function () {
            this.canSend =
                this.sendName.length && this.sendUrl.length && this.sendPrice.length >= 1;
            this.isButtonDisabled = !this.canSend;
        },
        sendPrice: function () {
            this.canSend =
                this.sendName.length && this.sendPrice.length && this.sendUrl.length >= 1;
            this.isButtonDisabled = !this.canSend;
        },
    },

    props: {
        msg: String,
    },

    methods: {
        log: function () {
            console.log('click');
        },
        someAction() {
            if (this.isPriceValid === true) {
                !this.submitValid;
            }
            alert('Форма отправлена');
        },
    },
};
</script>

<style>
form {
    background: #fffefb;
    width: 332px;
    max-height: 440px;
    border-radius: 4px;
    font-size: 1rem;
    display: flex;
    flex-direction: column;
    padding: 4px 14px 50px;
    color: #49485e;
}

.wrap {
    padding: 16px 0 0 0;
    width: 100%;
    text-align: left;
    font-size: 1rem;
}

button {
    border: 0px solid;
    padding: 10px 16px;
    width: 100%;
    border-radius: 10px;
    font-size: 0.8rem;
    background: #7bae73;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
    font-weight: 600;
    cursor: pointer;
    color: #ffffff;
}

button:disabled {
    background: #eeeeee;
    color: #b4b4b4;
}
textarea {
    border: 0px solid;
    padding: 10px 16px;
    width: 100%;
    box-sizing: border-box;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
    font-size: 1.1rem;
}

input {
    border: 0px solid;
    padding: 10px 16px;
    width: 100%;
    box-sizing: border-box;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
    font-size: 1.1rem;
}

input:optional {
    border-color: blue;
}
input:invalid {
    border: 2px solid #ff8484;
}

input:required::after {
    border: 2px solid green;
}

.field {
    margin-bottom: 24px;
}

.field > label {
    margin-right: 8px;
}

.error {
    border: 1px solid;
    border-color: #ff8484;
}

.activeBtn {
    border: 1px solid;
    border-color: green;
}

.errorField {
    color: #ff8484;
}
</style>
