<template>
    <div>
        <footer class="footer">
            <DivFooterComponent></DivFooterComponent>
            <DivFooterComponent></DivFooterComponent>
            <DivFooterComponent></DivFooterComponent>
            <DivFooterComponent></DivFooterComponent>
            <DivFooterComponent></DivFooterComponent>
        </footer>
    </div>
</template>

<script>

import DivFooterComponent from "@/components/DivFooterComponent/DivFooter.vue"


export default {
    name: 'FooterComponent',
    components: {
        DivFooterComponent
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
        justify-content: center;
        background: var(--bg-footer);
    }

    .footer__div{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background: var(--bg-footer-first-item);
        border: var(--boder-first-item);
        margin-right: 31px;
    }

    .div-two{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background: var(--bg-footer-second-item);
        border: var(--border-second-item);
        margin-right: 31px;
    }

    .div-three{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background: var(--bg-footer-third-item);
        border: var(--border-third-item);
        margin-right: 31px;
    }

    .div-four{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background: var(--bg-footer-fourth-item);
        border: var(--border-fourth-item);
        margin-right: 31px;
    }

    .div-five{
        width: 100px;
        height: 100px;
        border-radius: 50%;
        background: var(--bg-footer-fifth-item);
        border: var(--border-fifth-item);
    }

    .footer__div:last-child{
        margin-right: 0;
    }
</style>