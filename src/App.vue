<template>
    <div class="app">
        <Header />
        <Main />
        <Footer />
    </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: { Header, Footer, Main }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
}
.app {
    font-family: 'Segoe UI', 'Calibri', 'Arial', 'Helvetica Neue', sans-serif;
    font-size: 14pt;
    color: #6b4a37;
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    background-image: url('./assets/20220316_210018_1647593121670.jpeg');
    min-width: 550px;
}
</style>