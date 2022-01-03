<template>
    <div>
        <div class="feets__container" :style="theStyle" @click="generator"></div>
    </div>
</template>

<script>

import {getRandomColor} from "@/services/services.js"

export default {
    data(){
        return{
            theStyle: {
                backgroundColor: '#DFC89A'
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
    .feets__container{
        width: 334px;
        height: 261px;
        margin-right: 142px;
        cursor: pointer;
    }
</style>