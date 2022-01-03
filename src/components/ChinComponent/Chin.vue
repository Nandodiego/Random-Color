<template>
    <div>
        <div class="main__chin">
            <DivRefactor
                class="chin__container"
                :width="divStyles.width"
                :height="divStyles.height"
                :bg="divStyles.backgroundColor"
                @changeBg="changeColor"
            />   
        </div>
    </div>
</template>

<script>

import { getRandomColor } from "@/services/services.js";
import DivRefactor from "@/refactor/DivRefactor.component.vue";

export default {
    name: 'ChinComponent',
    components: {
        DivRefactor
    },
    data(){
        return {
            divStyles: {
                backgroundColor: '#1F1E1E',
                width: '166',
                height: '107',
            }
        }
    },
    methods: {
        changeColor(){
            this.divStyles.backgroundColor = getRandomColor();
        }
    }
}
</script>

<style scoped>
    .main__chin{
        width: 480px;
        height: 200px;
        margin: 0 auto;
        margin-top: 70px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        background: var(--bg-chin-container);
    }

    .chin__container{
        cursor: pointer;
    }
</style>