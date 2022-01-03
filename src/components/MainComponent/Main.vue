<template>
    <div>
        <main class="main">
            <EyesComponent></EyesComponent>
            <MouthComponent></MouthComponent>
            <ChinComponent></ChinComponent>
            <FeetsComponent></FeetsComponent>
        </main>
    </div>
</template>

<script>
import EyesComponent from "@/components/EyesComponent/Eyes.vue"
import MouthComponent from "@/components/MouthComponent/Mouth.vue"
import ChinComponent from "@/components/ChinComponent/Chin.vue"
import FeetsComponent from "@/components/FeetsComponent/Feets.vue"

export default {
    name: 'MainComponent',
    components: {
        EyesComponent,
        MouthComponent,
        ChinComponent,
        FeetsComponent
    }
}
</script>

<style scoped>
    .main{
        margin-top: 60px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>