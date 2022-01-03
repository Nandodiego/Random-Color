<template>
    <div>
        <div class="main__mouth">
            <div class="mouth__container">
                <DivMouthComponent></DivMouthComponent>
                <DivMouthComponent></DivMouthComponent>
                <DivMouthComponent></DivMouthComponent>
            </div>
        </div>
    </div>
</template>

<script>

import DivMouthComponent from "@/components/DivMouthComponent/DivMouth.vue"

export default {
    name: 'MouthComponent',
    components: {
        DivMouthComponent
    }
}
</script>


<style scoped>
    .main__mouth{
        width: 1285px;
        height: 361px;
        background: var(--bg-mouth-container);
        margin-top: 70px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    .mouth__container{
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        width: 1138px;
        height: 268px;
        background: var(--bg-mouth-secondary-container);
    }
</style>