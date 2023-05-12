<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <HelloWorld msg="Welcome to Your Vue.js App" :imgs="imgs" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data() {
    return {
      imgs: [
        "https://t7.baidu.com/it/u=1595072465,3644073269&fm=193&f=GIF",
        "https://t7.baidu.com/it/u=4198287529,2774471735&fm=193&f=GIF",
        "https://t7.baidu.com/it/u=1956604245,3662848045&fm=193&f=GIF"
      ]
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
