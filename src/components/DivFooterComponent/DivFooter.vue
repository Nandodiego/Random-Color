<template>
    <div>
        <div class="footer__div" :style="theStyle" @click="generator"></div>
    </div>
</template>

<script>

import {getRandomColor} from "@/services/services.js"

export default {
    data(){
        return{
            theStyle: {
                backgroundColor: '',
                border: ''
            }
        }
    },
    methods: {
        generator(){
            this.theStyle.backgroundColor = getRandomColor();
            this.generator2()
        },
       generator2(){
            this.theStyle.border = '10px solid' + getRandomColor();
        }
    }
}
</script>

<style scoped>
    .footer__div{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background: var(--bg-footer-first-item);
        border: var(--boder-first-item);
        margin-right: 31px;
    }
</style>