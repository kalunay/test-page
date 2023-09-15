<script setup>
import NavTop from './header/NavTop.vue';
import HeaderText from './header/HeaderText.vue';
import { menu, title, subtitle, button } from "../constants";
import { ref } from 'vue';

const showPop = ref(0)

const changeShowPop = () => {
    console.log(showPop);
    return showPop;
}
</script>

<template> {{ showPop }}
    <header>
        <div class="container">
        <div class="header">
            <div class="header__top">
            <div class="header__menu">
                <span class="logo">pascal</span>
                <span>Меню</span>
                <NavTop :links="menu" />
            </div>
            <div class="d-flex">
                <a href="#">8 (812) 603-71-79</a>
                <img src="../../public/img/menu-04.png" class="mobile" alt="">
                <a href="#" class="btn-feedback" @click.prevent="changeShowPop">Обратный звонок</a>
            </div>
            </div>
            <div class="header__bottom">
                <HeaderText :title="title" :subtitle="subtitle" :button="button" />
            </div>
        </div>
        </div>
    </header>
</template>

<style scoped>
</style>