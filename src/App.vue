<template>
  <div>
    <!-- 头部 -->
    <Header></Header>
    <!-- 轮播图 -->
    <Carousel></Carousel>
    <!-- 主要内容 -->
    <Content></Content>
    <!-- 底部说明 -->
    <Footer></Footer>
    
  </div>
</template>

<script>

import Header from "./components/Header/index.vue"
import Carousel from "./components/Carousel/carousel.vue"
import Content from './components/Content/content.vue'
import Footer from "./components/Footer/footer.vue"
  export default {
    name: "",
    components: { Header,Carousel,Content,Footer}
}
</script>

<style lang="css" scoped>

</style>