<template>
    <div>
        <div class="main__mouth">
            <div class="mouth__container">
                <DivRefactor 
                    v-for="styles in divsStyles"
                    :key="styles.cc"
                    :width="styles.width"
                    :height="styles.height"
                    :bg="styles.backgroundColor"
                    :cc="styles.cc"
                    @changeBg="changeBgColor($event)"
                />
            </div>
        </div>
    </div>
</template>

<script>
import { getRandomColor } from "@/services/services.js";
import DivRefactor from "@/refactor/DivRefactor.component.vue";

export default {
    name: 'MouthComponent',
    components: {
        DivRefactor
    },
    data() {
        return {
            divsStyles: [
                {
                    cc:'was',
                    backgroundColor: '#9E2626',
                    width: '199',
                    height: '166',
                },
                {
                    cc:'33',
                    backgroundColor: '#FAF4F4',
                    width: '199',
                    height: '166',
                },
                {
                    cc:'44',
                    backgroundColor: '#B5D200',
                    width: '199',
                    height: '166',
                }
            ]
        }
    },
    methods: {
        changeBgColor(event) {
            const findIndex = this.divsStyles.findIndex(item => item.cc === event);
            if(findIndex > -1) {
                this.divsStyles[findIndex].backgroundColor = getRandomColor();
            }
        }
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
        justify-content: space-evenly;
        width: 1138px;
        height: 268px;
        background: var(--bg-mouth-secondary-container);
        cursor: pointer;
    }
</style>