<template>
    <div class="work-element">
        <div class="work-element__image-wrapper " :class="{ 'work-element__image-wrapper_with-arrow': arrow }">
            <img :src="require('../../assets/img/rounds/' + image + '.webp')" alt="">
        </div>
        <p>{{text}}</p>
    </div>
</template>

<script>
    export default {
        props: {
            arrow: {
                type: String,
                default: ''
            },
            text: {
                type: String,
                default: ''
            },
            image: {
                type: String,
                default: ''
            },
        },
    }
</script>

<style lang="scss" scoped>
.work-element {
    display: flex;
    flex-direction: column;
    align-items: center;

    &__image-wrapper {
        position: relative;
        width: 100px;
        height: 100px;
        margin-bottom: 15px;

        &_with-arrow {
            @media screen and (min-width: $MEDIA_TABLET_TO_DESKTOP) {
                position: relative;

                &::after {
                    position: absolute;
                    top: calc(50% - 7px);
                    left: calc(100% + 21px);
                    content: '';
                    width: 105px;
                    height: 14px;
                    background-image: url('./strelka.svg');
                }
            }
        }
    }

    & p {
        text-align: center;

        @media screen and (max-width: 800px) {
            font-size: 16px;
        }
    }
}
</style>