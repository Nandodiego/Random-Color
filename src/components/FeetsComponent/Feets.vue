<template>
    <div>
        <div class="main__feets">
            <DivFeetsComponent></DivFeetsComponent>
            <DivFeetsComponent></DivFeetsComponent>
            <DivFeetsComponent></DivFeetsComponent>
        </div>
    </div>
</template>

<script>

import DivFeetsComponent from "@/components/DivFeetsComponent/DivFeets.vue"

export default {
    name: 'FeetsComponent',
    components: {
        DivFeetsComponent
    }
}
</script>

<style scoped>
    .main__feets{
        width: 1285px;
        height: 361px;
        margin-top: 124px;
        background: var(--bg-feets-container);
        display: flex;
        flex-direction: row;
    }
</style>