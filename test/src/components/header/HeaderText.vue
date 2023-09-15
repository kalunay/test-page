<script setup>
import ModalVuew from '../../components/UI/ModalVuew.vue';
import { ref } from 'vue';

const props = defineProps({
    title: {
        type: String,
        required: true 
    },
    subtitle: {
        type: String,
        required: true 
    },
    button: {
        type: String,
        default: 'Получить бесплатную консультацию' 
    }
});

const showPop = ref(false);

const closePopUp = () => {
    return showPop.value = !showPop.value;
}
</script>

<template>
    <h1>{{ title }}</h1>
    <p>{{ subtitle }}</p>
    <a href="" class="btn" @click.prevent="showPop = !showPop">{{ button }}</a>
    
    <Teleport to="body">
        <ModalVuew :hide="showPop" @closePopUp="closePopUp" />
    </Teleport>
</template>