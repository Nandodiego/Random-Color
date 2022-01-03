<template>
    <div>
        <div class="main__eyes">
            <DivEyeComponent></DivEyeComponent>
            <DivEyeComponent></DivEyeComponent>
        </div>
    </div>
</template>

<script>

import DivEyeComponent from "@/components/DivEyeComponent/DivEye.vue"

export default {
    name: 'EyesComponent',
    components: {
        DivEyeComponent
    }
}
</script>

<style scoped>
    .main__eyes{
        width: 1285px;
        background: var(--bg-eyes-container);
        height: 361px;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 0px 50px 0px 50px;
    }
</style>