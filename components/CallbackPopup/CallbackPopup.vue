<template>
    <form class="callback-popup" @click.stop v-if="callbackPopupIsOpen">
        <button class="callback-popup__close" @click.prevent="closeCallbackPopup"/>
        <p class="callback-popup__header">Оставьте заявку</p>
        <p class="callback-popup__subheader">Чтобы получить консультацию или сделать заказ</p>
        <input type="text" name="name" placeholder="Ваше имя*" class="callback-popup__input">
        <input type="text" name="phone" placeholder="Ваш телефон*" class="callback-popup__input">
        <textarea name="description" cols="30" rows="3" placeholder="Описание объекта" class="callback-popup__textarea"></textarea>
        <input type="submit" value="Получить консультацию" class="callback-popup__submit">
        <p class="callback-popup__agreement">Оставляя заявку, Вы соглашаетесь на обработку персональных данных. Ваши данные ни в коем случае не будут переданы третьим лицам.</p>
    </form>
</template>

<script>
    export default {
        computed: {
            callbackPopupIsOpen() {
            return this.$store.state.popups.callbackPopupIsOpen 
            }
        },
        methods: {
            closeCallbackPopup() {
                this.$store.commit('popups/closeCallbackPopup')
            }
        },
    }
</script>

<style lang="scss" scoped>
.callback-popup {
    position: relative;
    width: 400px;
    padding: 30px;
    display: flex;
    flex-direction: column;
    background-color: #fff;
    border-radius: 6px;

    @media screen and (max-width: $MEDIA_TABLET_TO_MOBILE) {
        width: 100%;
        height: 100%;
        padding: 60px 15px 30px;
    }

    &__header {
        margin-bottom: 10px;
        font-size: 28px;
        text-align: center;
    }

    &__subheader {
        margin-bottom: 30px;
        font-size: 20px;
        text-align: center;
    }

    &__submit {
        font-size: 20px;
        height: 45px;
        background-color: #6eafff;
        color: #fff;
        border-width: 0;
        border-radius: 8px;
        text-transform: uppercase;
        box-shadow: 2px 2px 8px 0px rgb(0 0 0 / 30%);
        cursor: pointer;
        font-weight: bold;
        transition: background-color 0.3s ease;

        &:hover{
            background-color: #6e8dff;
        }

        @media screen and (max-width: $MEDIA_TABLET_TO_MOBILE) {
            font-size: 18px;
        }

        @media screen and (max-width: 359px) {
            font-size: 16px;
        }
    }

    &__input {
        height: 40px;
        margin-bottom: 15px;
        padding: 2px 3px;
        font-size: 20px;
    }

    &__textarea {
        margin-bottom: 25px;
        padding: 2px 3px;
        resize: none;
        font-size: 14px;
    }

    &__agreement {
        font-size: 12px;
        margin: 20px 0 0;
        text-align: center;
    }

    &__close {
        position: absolute;
        right: 15px;
        top: 15px;
        height: 30px;
        width: 30px;
        opacity: 0.5;
        transition: all 0.3s ease;
        border: unset;
        background-color: transparent;
        cursor: pointer;

        &:hover {
            opacity: 1;
        }
        
        &::after,
        &::before {
            content: "";
            position: absolute;
            top: 14px;
            left: 0;
            width: 30px;
            height: 2px;
            background: black;
        }

        &::after {
            transform: rotate(45deg);
        }

        &::before {
            transform: rotate(-45deg);
        }
    }
}
</style>