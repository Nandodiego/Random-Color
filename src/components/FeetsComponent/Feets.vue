<template>
    <div>
        <div class="main__feets">
            <DivRefactor
                class="feets__container"
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
    name: 'FeetsComponent',
    components: {
        DivRefactor
    },
    data(){
        return {
            divsStyles: [
                {
                    cc: "ds8a",
                    backgroundColor: '#DFC89A',
                    width: '334',
                    height: '261',
                },
                {
                    cc: "dsa2",
                    backgroundColor: '#DFC89A',
                    width: '315',
                    height: '268',
                },
                {
                    cc: "dsa3",
                    backgroundColor: '#DFC89A',
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
    .main__feets{
        width: 1285px;
        height: 361px;
        margin-top: 124px;
        background: var(--bg-feets-container);
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    .feets__container{
        cursor: pointer;
    }
</style>