<template>
    <header class="header">
        <h1 class="heading">
            <img :src="LogoImg" alt="Логотип" class="logo">
            Курс &laquo;Создание брошей&raquo;
        </h1>
        <button class="burger" id="btn">
            <img src="../assets/burger3.svg" alt="Меню" title="Меню" width="30" height="30"/>
        </button>
    </header>
</template>

<script>
import LogoImg from '../assets/лого.png'

export default {
  name: 'Header',
  data: () => ({
    LogoImg
  }),
}
</script>

<style>
.header::before {
    content: '';
    display: block;
    width: 200px;
    background: radial-gradient(ellipse at top 0 right 0, rgba(255,255,255,1) 42%, rgba(255,255,255,0) 70%);
    height: 100%;
    position: absolute;
    left: -200px;
    top: 0;
}
.header::after {
    content: '';
    display: block;
    width: 150px;
    background: radial-gradient(ellipse at top 0 left 0, rgba(255,255,255,1) 42%, rgba(255,255,255,0) 70%);
    height: 100%;
    position: absolute;
    right: -150px;
    top: 0;
}
.header {
    display: flex;
    padding: 15px 0;
    justify-content: space-between;
    align-items: flex-start;
    background: linear-gradient(180deg, rgba(255,255,255,1) 60%, rgba(255,255,255,0));
    margin: 0 auto;
    max-width: 1150px;
    position: relative;
}
.heading {
    font-size: 18pt;
    display: flex;
    align-items: flex-start;
}
.header-link {
    text-decoration: none;
    color: inherit;
}
.logo {
    width: 125px;
    margin-right: 20px;
}
.burger {
    background-color: inherit;
    border: none;
    outline-width: 0;
    transition: 0.1s all ease-in;
    margin-right: 20px;
}
.burger:hover {
    transform: scale(1.2);
}
</style>