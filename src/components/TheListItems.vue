<template>
    <div class="wrap">
        <div class="container">
            <div v-for="item in ItemsArr" :key="item.id">
                <CardItem
                    :title="item.title"
                    :text="item.text"
                    :image="item.image"
                    :price="item.price"
                />
            </div>
        </div>
    </div>
</template>

<script>
import CardItem from './CardItem.vue';
import CardImage from '../assets/logo.png';

export default {
    name: 'theListItems',
    components: { CardItem },
    data() {
        return {
            ItemsArr: [
                {
                    title: 'Наименование товара',
                    text: 'Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк',
                    image: CardImage,
                    price: 100,
                    id: '1',
                },
                {
                    title: 'Наименование товара',
                    text: 'Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк',
                    image: CardImage,
                    price: 120,
                    id: '2',
                },
                {
                    title: 'Наименование товара',
                    text: 'Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк',
                    image: CardImage,
                    price: 420,
                    id: '3',
                },
                {
                    title: 'Наименование товара',
                    text: 'Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк',
                    image: CardImage,
                    price: 240,
                    id: '4',
                },
                {
                    title: 'Наименование товара',
                    text: 'Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк',
                    image: CardImage,
                    price: 300,
                    id: '5',
                },
                {
                    title: 'Наименование товара',
                    text: 'Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк',
                    image: CardImage,
                    price: 90,
                    id: '6',
                },
            ],
        };
    },
};
</script>
<style>
.wrap {
    /* width: 100%; */
    height: 100%;
}
.container {
    background: #fffefb;
    padding: 25px;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    /* grid-template-rows: repeat(2, 1fr); */
    /* grid-column-gap: 11px; */

    /* grid-auto-rows: minmax(350px, auto); */
    grid-gap: 0.5rem;
}
@media (max-width: 1400px) {
    .container {
        grid-template-columns: repeat(3, 1fr);
    }
}

@media (max-width: 1050px) {
    .container {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (max-width: 690px) {
    .container {
        grid-template-columns: repeat(1, 1fr);
    }
}
</style>
