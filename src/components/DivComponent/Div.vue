<template>
    <div>
        <div class="container__div" :style="theStyle" @click="generator"></div>
    </div>
</template>

<script>

import {getRandomColor} from "@/services/services.js"

export default {
    data(){
        return {
            theStyle: {
                backgroundColor: '',
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
        cursor: pointer;
        Width: 242px;
        Height: 87px;
        margin-right: 50px;
        background: var(--bg-items-header);
    }

    .header__div:last-child{
        margin-right: 0;
    }
    
    .isActive{
        background: red;
    }
</style>