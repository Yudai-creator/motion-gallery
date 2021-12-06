<template name="component-name">
    <div class="circle">
        
    </div>
</template>
<script>
// JS
export default {
    
}
</script>
<style lang="scss">
@import '~assets/scss/variables';

    .circle{
        width: 35px;
        height: 35px;
        border: 3px solid $secondary;
        border-radius: 50%;

        position: absolute;
        z-index: -1;
    }

</style>