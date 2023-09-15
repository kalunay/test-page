<script setup>
import { useVuelidate } from '@vuelidate/core';
import { helpers, required } from '@vuelidate/validators';
import { ref, computed } from 'vue';

const props = defineProps({
    hide: {
        type: Boolean,
        default: false
    }
});

const nameField = ref('');
const phoneField = ref('');
const msg = ref('');

const rules = computed(() => ({
  nameField: {
    required: helpers.withMessage(`Обязательно для заполнения!`, required)
  },
  phoneField: {
    required: helpers.withMessage(`Обязательно для заполнения!`, required)
  }
}));

const v = useVuelidate(rules, {nameField, phoneField})

const submitForm = () => {
  v.value.$touch()
  if (v.value.$error) return
  msg.value = 'Сообщение отправлено!'
}

const emit = defineEmits(['closePopUp']);
const clickOnButton = () => {
    emit('closePopUp');
}
</script>

<template>
    <div :class="['modal', {'active': hide}]">
        <div class="modal__wrap">
            <div class="modal__header">Оставьте заявку и мы перезвоним</div>
            <span v-if="msg">{{ msg }}</span>
            <form action="" @submit.prevent="submitForm">
                <div class="modal__form">
                    <div class="feedback__field">
                        <label for="">Имя</label>
                        <input type="text" placeholder="Иван" v-model="v.nameField.$model" />
                        <span v-if="v.nameField.$errors.length > 0">{{ v.nameField.$errors[0].$message }}</span>
                    </div>
                    <div class="feedback__field">
                        <label for="">Телефон</label>
                        <input type="tel" placeholder="+7" v-model="v.phoneField.$model" />            
                        <span v-if="v.phoneField.$errors.length > 0">{{ v.phoneField.$errors[0].$message }}</span>
                    </div>      
                    <div class="modal_footer">
                        <p>Нажимая на кнопку, я даю согласие на обработку персональных данных в соответствии с Политикой конфиденциальности</p>
                        <button type="submit">Отправить</button>
                    </div>
                </div>            
            </form>

            <a href="#" @click.prevent="clickOnButton" class="btn-close"></a>        
        </div>
    </div>
</template>