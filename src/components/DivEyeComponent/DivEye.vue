<template>
    <div>
        <div class="div__eye" :style="theStyle" @click="generator"></div>
    </div>
</template>

<script>

import {getRandomColor} from "@/services/services.js"

export default {
    data(){
        return{
            theStyle: {
                backgroundColor: ''
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
    .div__eye{
        cursor: pointer;
        width: 315px;
        height: 268px;
        background: var(--bg-eyes-items);
    }
</style>