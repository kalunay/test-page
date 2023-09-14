<script setup>
import NavTop from './header/NavTop.vue';
import { menuBottom, links } from "../constants";
</script>

<template>
    <footer>
    <div class="container">
        <div class="footer__widgets">
        <span class="logo">pascal</span>
        <NavTop :links="menuBottom" class="footer__menu" />
        <div class="footer__socials__phone">
            <div>
            <a href="tel:88126037179" class="btn-phone">8 (812) 603-71-79</a>
            <a href="" class="btn-feedback2">Обратный звонок</a>
            </div>  
            <div class="footer__socials">
            <a href="#">&nbsp;</a>
            <a href="#">&nbsp;</a>
            <a href="#">&nbsp;</a>
            <a href="#">&nbsp;</a>
            <a href="#">&nbsp;</a>
            </div>
        </div>
        </div>
        <div class="footer__links">
            <template v-for="link in links" :key="link.id">
                <a :href="link.link" :class="{'active' : link.id == 7 }">{{ link.name }}</a>
            </template>
        </div>
    </div>
    </footer>
</template>