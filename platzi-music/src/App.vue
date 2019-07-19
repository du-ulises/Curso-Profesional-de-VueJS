<template lang="pug">
  #app
    search
    sideBar
    movieCards
</template>

<script>
import Search from'./components/search/Search.vue'
import SideBar from'./components/sideBar/SideBar.vue'
import movieCards from'./components/movieCards/movieCards.vue'
export default {
  name: 'app',
  data () {
    return {
      msg: 'Hello World'
    }
  },
  components: {
    Search,
    SideBar,
    movieCards
  }
}
</script>

<style lang="scss">
  @import './scss/main.scss';
  #app {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
