<template>
    <div>
        <div 
            :style="{
                width: width + 'px',
                height: height + 'px',
                backgroundColor: bg,
                border: borderDiv,
                borderRadius: borderRadiusDiv + '%'
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
        },
        borderDiv: {
            type: String
        },
        borderRadiusDiv: {
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