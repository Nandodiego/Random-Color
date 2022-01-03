<template>
    <div>
        <div class="container__div" :style="theStyle" @click="generator"></div>
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
    .container__div{
        width: 200px;
        height: 166px;
        margin-right: 90px;
        cursor: pointer;
        background: var(--bg-mouth-items);
    }

</style>