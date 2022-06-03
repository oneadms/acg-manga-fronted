<template>
  <div style="width: 85%;margin: auto;border: solid #e8e8e8 1px;">
    <Header></Header>
    <Nuxt></Nuxt>
    <Content></Content>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import Content from '../components/Content.vue'
import Footer from '../components/Footer.vue'
export default {
  name: 'Home',
  components: { Footer, Content, Header }
}
</script>

<style scoped>

</style>
