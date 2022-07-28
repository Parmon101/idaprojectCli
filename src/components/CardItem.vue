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
    max-width: 332px;
    max-height: 440px;
    border-radius: 4px;
    display: flex;
    flex-direction: column;
    padding: 4px 14px 50px;
    color: #49485e;
    cursor: pointer;
}

.card:hover {
    /* background: red; */
}

.card-content {
    padding: 0 16px 24px 16px;
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
.wrapp {
    padding: 16px 0 0 0;
    width: 100%;
    text-align: left;
    font-size: 1rem;
    background: red;
}
</style>
