<template>
    <div>
        <div class="main__chin">
            <div class="chin__container" :style="theStyle" @click="generator"></div>
        </div>
    </div>
</template>

<script>

import {getRandomColor} from "@/services/services.js"

export default {
    name: 'ChinComponent',
    data(){
        return {
            theStyle: {
                backgroundColor: '#1F1E1E'
            }
        }
    },
    methods: {
        generator(){
            this.theStyle.backgroundColor = getRandomColor();
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
        width: 166px;
        height: 107px;
        cursor: pointer;
    }
</style>