<template>
    <div class="home">
        <div class="container">
            <div class="split">
                <Form />
                <TheListItems />
            </div>
        </div>
    </div>
</template>

<script>
import Form from './Form.vue';
import TheListItems from './TheListItems.vue';

export default {
    name: 'HelloWorld',
    components: {
        Form,
        TheListItems,
    },
    props: {
        msg: String,
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
}
.split {
    display: flex;
}
h3 {
    margin: 40px 0 0;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: inline-block;
    margin: 0 10px;
}
a {
    color: #42b983;
}
</style>
