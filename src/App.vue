<template>
  <div class="container-fluid">
    <HeaderComponent/>
    <MainComponent/>
    <ThirdSection/>
  </div>
  
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import MainComponent from './components/MainComponent.vue'
import ThirdSection from './components/ThirdSection.vue'
export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    ThirdSection
  },
}
</script>

<style>
@import "./assets/app.css";
</style>
