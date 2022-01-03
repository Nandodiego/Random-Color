<template>
    <div>
        <footer class="footer">
            <div class="footer__container">
                <DivRefactor 
                class="container__div"
                v-for="styles in divsStyles"
                :key="styles.cc"
                :width="styles.width"
                :height="styles.height"
                :bg="styles.backgroundColor"
                :cc="styles.cc"
                :borderDiv="styles.border"
                :borderRadiusDiv="styles.borderRadiusDiv"
                @changeBg="changeColor($event)"
                />
            </div>
        </footer>
    </div>
</template>

<script>

import { getRandomColor } from "@/services/services.js";
import DivRefactor from "@/refactor/DivRefactor.component.vue";

export default {
    name: 'FooterComponent',
    components: {
        DivRefactor
    },
    data(){
        return {
            divsStyles: [
                {
                    cc: "ds8a",
                    backgroundColor: '#E42424',
                    width: '100',
                    height: '100',
                    border: '10px solid #3A49D3',
                    borderRadiusDiv: '50'
                },
                {
                    cc: "dsa2",
                    backgroundColor: '#D0BBD3',
                    width: '100',
                    height: '100',
                    border: '10px solid #0E0E0E',
                    borderRadiusDiv: '50'
                },
                {
                    cc: "dsa4",
                    backgroundColor: '#62E424',
                    width: '100',
                    height: '100',
                    border: '10px solid #000000',
                    borderRadiusDiv: '50'
                },
                {  
                    cc: "dsa5",
                    backgroundColor: '#CBAAAA',
                    width: '100',
                    height: '100',
                    border: '10px solid #000000',
                    borderRadiusDiv: '50'
                },
                {  
                    cc: "dsa9",
                    backgroundColor: '#4F71EA',
                    width: '100',
                    height: '100',
                    border: '10px solid #E1D13D',
                    borderRadiusDiv: '50'
                }
            ]
        }
    },
    methods: {
        changeColor(event){
            const findIndex = this.divsStyles.findIndex(item => item.cc === event);
            if(findIndex > -1) {
                this.divsStyles[findIndex].backgroundColor = getRandomColor();
                this.getBorderColor(event)
            }
        },
        getBorderColor(event){
            const findIndex = this.divsStyles.findIndex(item => item.cc === event);
            if(findIndex > -1) {
                this.divsStyles[findIndex].border ='10px solid' + getRandomColor();    
            }
        }
    }
}
</script>

<style scoped>
    .footer{
        width: 100%;
        height: 176px;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-around;
        background: var(--bg-footer);
    }

    .footer__container{
        display: flex;
        width: 650px;
        justify-content: space-around;
    }

    .container__div{
        cursor: pointer;
    }
</style>