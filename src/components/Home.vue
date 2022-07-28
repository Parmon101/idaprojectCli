<template>
    <div class="home">
        Home Page
        <TheListItems/>
    </div>
</template>

<script>
import TheListItems from './TheListItems.vue';

export default {
    name: 'HelloWorld',
    components: {
    TheListItems
},
    props: {
        msg: String,
    },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
