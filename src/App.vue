<template>
    <div id="app">
        <Hero msg="Welcome to Your Vue.js App"/>
        <img alt="Vue logo" src="./assets/logo.png">
        <HelloWorld msg="Welcome to Your Vue.js App"/>


    </div>
</template>

<script>
    import Vue from 'vue'
    import BootstrapVue from 'bootstrap-vue'
    import 'bootstrap/dist/css/bootstrap.css'
    import 'bootstrap-vue/dist/bootstrap-vue.css'


    Vue.use(BootstrapVue);
    import HelloWorld from './components/HelloWorld.vue'
    import Hero from './components/Hero.vue'


    export default {
        name: 'app',
        components: {
            Hero,
            HelloWorld
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
