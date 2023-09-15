<script setup>
import { useVuelidate } from '@vuelidate/core'
import { required, email } from '@vuelidate/validators'
</script>

<template>
    <div class="modal">
        <div class="modal__wrap">
            <div class="modal__header">Оставьте заявку и мы перезвоним</div>

            <div class="modal__form">
            <div class="feedback__field">
                <label for="">Имя</label>
                <input type="text" placeholder="Иван" />
            </div>
            <div class="feedback__field">
                <label for="">Телефон</label>
                <input type="text" placeholder="+7" />
            </div>      
            </div>
            <div class="modal_footer">
            <p>Нажимая на кнопку, я даю согласие на обработку персональных данных в соответствии с Политикой конфиденциальности</p>
            <button type="submit">Отправить</button>
            </div>

            <a href="#" class="btn-close"></a>        
        </div>
    </div>
</template>