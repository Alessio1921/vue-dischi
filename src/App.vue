<template>
  <div id="app">
    <Header />
    <CardList />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import CardList from './components/CardList.vue'
import axios from 'axios'

export default {
  name: 'App',
  components: {
    Header,
    CardList
  },
  data:function(){
    return{
      info:null
    }
  },
  methods:{
    
  },
  mounted() {
    axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(response => (this.info = response))
  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap";
#app {
  // font-family: Avenir, Helvetica, Arial, sans-serif;
  // -webkit-font-smoothing: antialiased;
  // -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  // color: #2c3e50;
  // margin-top: 60px;
}
</style>
