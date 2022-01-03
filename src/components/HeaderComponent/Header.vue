<template>
    <div>
        <header class="header">
            <DivRefactor 
                class="div__container"
                v-for="styles in divsStyles"
                :key="styles.cc"
                :width="styles.width"
                :height="styles.height"
                :bg="styles.backgroundColor"
                :cc="styles.cc"
                @changeBg="changeColor($event)"
            />
        </header>
    </div>
</template>

<script>

import { getRandomColor } from "@/services/services.js";
import DivRefactor from "@/refactor/DivRefactor.component.vue";


export default {
    name: 'HeaderComponent',
    components: {
        DivRefactor
    },
    data(){
        return {
            divsStyles: [
                {
                    cc: "ds8a",
                    backgroundColor: '#F4FBFC',
                    width: '242',
                    height: '87',
                },
                {
                    cc: "dsa2",
                    backgroundColor: '#F4FBFC',
                    width: '242',
                    height: '87',
                },
                {
                    cc: "dsa4",
                    backgroundColor: '#F4FBFC',
                    width: '242',
                    height: '87',
                },
                {  
                    cc: "dsa5",
                    backgroundColor: '#F4FBFC',
                    width: '242',
                    height: '87',
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
    .header{
        background: var(--bg-header);
        width: 100%;
        height: 159px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-evenly;
    }

    .div__container{
        cursor: pointer;
    }
</style>