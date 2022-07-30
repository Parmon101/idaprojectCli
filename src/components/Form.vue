<template>
    <div class="form">
        <h2>Добавление товара</h2>
        <div class="wrap">
            <article>
                <span>
                    <pub>Наименование товара</pub>
                    <img alt="red" src="../assets/red.svg" />
                </span>
            </article>
            <input type="text" placeholder="Введите наименование товара" />
        </div>

        <div class="wrap">
            <article>
                <pub>Описание товара</pub>
                <img alt="red" src="../assets/red.svg" />
            </article>
            <textarea name="" id="" cols="30" rows="10" placeholder="Введите описание"> </textarea>
        </div>

        <div class="wrap">
            <article>
                <pub>Ссылка на изображение товара</pub>
                <img alt="red" src="../assets/red.svg" />
            </article>
            <input type="text" placeholder="Введите ссылку" />
        </div>

        <div class="wrap">
            <article>
                <pub>Цена товара</pub>
                <img alt="red" src="../assets/red.svg" />
            </article>
            <input type="text" placeholder="Введите цену" />
        </div>

        <div class="wrap">
            <button v-on:click="log">Добавить товар</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'HomeForm',
    props: {
        msg: String,
    },

    methods: {
        log: function () {
            console.log('click');
        },
    },
};
</script>

<style>
.form {
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
    background: #eeeeee;
    font-weight: 600;
    cursor: pointer;
}

textarea {
    border: 0px solid;
    padding: 10px 16px;
    width: 100%;
    box-sizing: border-box;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
    background: #fffefb;
}

input {
    border: 0px solid;
    padding: 10px 16px;
    width: 100%;
    box-sizing: border-box;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
}
</style>
