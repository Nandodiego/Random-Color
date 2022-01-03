<template>
    <div>
        <header class="header">
            <DivComponent></DivComponent>
            <DivComponent></DivComponent>
            <DivComponent></DivComponent>
            <DivComponent></DivComponent>
        </header>
    </div>
</template>

<script>
import DivComponent from "@/components/DivComponent/Div.vue"

export default {
    name: 'HeaderComponent',
    components: {
        DivComponent
    }
}
</script>

<style scoped>
    .header{
        background: var(--bg-header);
        width: 100%;
        height: 159px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }
</style>