<template>
  <div  >
    <!-- <h1>{{ msg }}</h1> -->
    <!-- <ul>
      <li v-for="(item,index) in imgs" :key="index" ><a href="item" target="_blank" rel="noopener"><img :src="item" /></a></li>
    </ul> -->
    <masonry-wall id="lightgallery" :items="imgs" :rtl="false" :ssr-columns="1" :column-width="300" :gap="1">
      <template #default="{ item, index }">
        <div v-if="!item.filted" style=" " class="itemzximgbox lightgallerysrc" :data-src="item"
          :data-index="index">
          <a :href="item" target="_blank" rel="noopener"><img class="iimg"  :data-src="item" :src="item" /></a>
        </div>
      </template>
    </masonry-wall>
  </div>
</template>

<script>
import MasonryWall from "vue-masonry-wall";
  export default {
    name: 'HelloWorld',
    components: {
      MasonryWall,
      // Lightgallery,
    },
    props: {
      msg: String,
      imgs: Array,
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
img{
      width: 100%;
    height: 100%;
}
  h3 {
    margin: 40px 0 0;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>