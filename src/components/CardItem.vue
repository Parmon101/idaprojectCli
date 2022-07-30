<template>
    <div class="cart">
        <article class="card">
            <picture class="thumbnail">
                <img class="category__01" src="../assets/logo.png" alt="" />
            </picture>
            <div class="card-content">
                <h2>{{ title }}</h2>
                <p>
                    {{ text }}
                </p>
                <div class="price">{{ price }} руб</div>
            </div>
        </article>
    </div>
</template>

<script>
export default {
    name: 'cartItem',
    props: {
        title: String,
        text: String,
        image: String,
        price: Number,
    },
};
</script>

<style>
.cart {
    background: #fffefb;
    width: 332px;
    border-radius: 4px;
    display: flex;
    flex-direction: column;
    color: #49485e;
    cursor: pointer;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
}

.card:hover {
    /* background: red; */
}

.card-content {
    padding: 0 5px 20px 5px;
    text-align: left;
    color: #3f3f3f;
}

.card-content > h2 {
    font-size: 1.2rem;
}

.card-content > p {
    font-size: 0.9rem;
}

.card-content > .price {
    font-weight: 600;
    font-size: 1.3rem;
}

.category__01 {
    display: block;
    margin-left: auto;
    margin-right: auto;
}
.wrapp {
    padding: 16px 0 0 0;
    width: 100%;
    text-align: left;
    font-size: 1rem;
    background: red;
}
</style>
