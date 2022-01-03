<template>
    <div>
        <div 
            :style="{
                width: width + 'px',
                height: height + 'px',
                backgroundColor: bg
            }" 
            @click="changeColor"
        ></div>
    </div>
</template>

<script>

export default {
    name: 'refactorComponent',
    props: {
        width: {
            type: String
        },
        height: {
            type: String
        },
        bg: {
            type: String,
            default: '#ffffff'
        },
        cc: {
            type: String
        }
    },
    methods: {
        changeColor(){
            this.$emit('changeBg', this.cc);
        }
    }
}
</script>