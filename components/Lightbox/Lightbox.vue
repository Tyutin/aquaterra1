<template>
    <div class="lightbox">
        <slot />
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
.lightbox {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10;
    background-color: #00000066;
}
</style>