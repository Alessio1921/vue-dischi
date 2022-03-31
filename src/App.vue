<template>
  <div id="app">
    <Header @select="userSelect"/>
    <!-- <h2>{{selected}}</h2> -->
    <CardList :userSelected="selected" />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import CardList from './components/CardList.vue'

export default {
  name: 'App',
  components: {
    Header,
    CardList
  },
  data:function(){
    return{
      selected:""
    }
  },
  methods:{
    userSelect(value){
      this.selected=value;
      console.log(this.selected);
    }
  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap";

</style>
