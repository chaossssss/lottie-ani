<template>
  <div class="home">
    <div id="container" class="container"></div>
  </div>
</template>

<script>
import lottie from 'lottie-web'
import animationData from '../assets/data.json'
export default {
  name: 'Home',
  mounted() {
    this.init()
  },
  methods: {
    init() {
      lottie.loadAnimation({
        container: document.getElementById("container"), // the dom element
        renderer: 'svg',
        loop: true,
        autoplay: true,
        animationData: animationData, // the animation data
      });
    }
  }
}
</script>
<style>
.container {
  width: 800px;
  height: 600px;
}
</style>