<template>
  <div>
      <HeaderComponent></HeaderComponent>
      <MainComponent></MainComponent>
      <FooterComponent></FooterComponent>
  </div>
</template>

<script>

import HeaderComponent from "@/components/HeaderComponent/Header.vue"
import MainComponent from "@/components/MainComponent/Main.vue"
import FooterComponent from "@/components/FooterComponent/Footer.vue"


export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent
  }
}
</script>

<style>
  *{
    padding: 0;
    margin: 0;
    box-sizing: border-box;
  }

  :root{
    --bg-header: #3F31E2;
    --bg-items-header: #F4FBFC;
    --bg-eyes-container: #BC73DE;
    --bg-eyes-items: #3D3838;
    --bg-mouth-container: #BC73DE;
    --bg-mouth-secondary-container: #3D3838;
    --bg-mouth-items: #FAF4F4;
    --bg-chin-container: #BC73DE;
    --bg-chin-item: #1F1E1E;
    --bg-feets-container: #FFFFFF;
    --bg-feets-items: #DFC89A;
    --bg-footer: #F4F0F0;
    --bg-footer-first-item: #E42424;
    --boder-first-item: 10px solid #3A49D3;
    --bg-footer-second-item: #D0BBD3;
    --border-second-item: 10px solid #0E0E0E;
    --bg-footer-third-item: #62E424;
    --border-third-item: 10px solid #311919;
    --bg-footer-fourth-item: #CBAAAA;
    --border-fourth-item: 10px solid #000000;
    --bg-footer-fifth-item: #4F71EA;
    --border-fifth-item: 10px solid  #E1D13D;
  }
</style>
