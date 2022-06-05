<template>
    <section class="callback-section">
        <Callback />
    </section>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
.callback-section {
    position: relative;
    padding: 40px 0;
    background-color: $COLOR_BLUE_H1;

        @media screen and (max-width:$MEDIA_DESKTOP_TO_TABLET) {
            padding: 30px 0;
        }

    &::after, &::before {
        position: absolute;
        content: "";
        width: 100%;
        height: 20px;
        background-image: url('./wave.svg');
        z-index: 1;
    }
    &::after {
        bottom: -10px;
    }
    &::before {
        top: -10px;
        transform: rotate(180deg);
    }
}
</style>