<template>
    <div>
        <div class="main__eyes">
            <DivRefactor
                class="eyes__container"
                v-for="styles in divsStyles"
                :key="styles.cc"
                :width="styles.width"
                :height="styles.height"
                :bg="styles.backgroundColor"
                :cc="styles.cc"
                @changeBg="changeColor($event)"
            />
        </div>
    </div>
</template>

<script>

import { getRandomColor } from "@/services/services.js";
import DivRefactor from "@/refactor/DivRefactor.component.vue";

export default {
    name: 'EyesComponent',
    components: {
        DivRefactor
    },
    data(){
        return {
            divsStyles: [
                {
                    cc: "ds8a",
                    backgroundColor: '#3D3838',
                    width: '315',
                    height: '268',
                },
                {
                    cc: "dsa2",
                    backgroundColor: '#3D3838',
                    width: '315',
                    height: '268',
                },
            ]
        }
    },
    methods: {
        changeColor(event){
            const findIndex = this.divsStyles.findIndex(item => item.cc === event);
            if(findIndex > -1) {
                this.divsStyles[findIndex].backgroundColor = getRandomColor();
            }
        }
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

    .eyes__container{
        cursor: pointer;
    }
</style>