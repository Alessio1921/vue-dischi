<template>
  <main class="pb-5">
    <div class="container">
      <div class="row row-cols-3 row-cols-md-4 row-cols-lg-5 row-cols-xl-6" v-if="elementList">
        <div class="col" v-for="(element,index) in elementList" :key="index">
          <Card 
            :card="element"
          />
        </div>
      </div>
      <div class="loader d-flex justify-content-center" v-else> <Loader /></div>
    </div>
  </main>
</template>

<script>
import Card from './Card.vue'
import Loader from './Loader.vue'
import axios from 'axios'

export default {
  components: { Card,
  Loader
  },
  name: 'CardList',
  data:function(){
    return{
      elementList:null
    }
  },
  methods:{
    getApi(){
      axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(response => (this.elementList = response.data.response))
      .catch(error => {
        console.log(error)
      })
    }
  },
  mounted() {
    setTimeout(this.getApi,2000)
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  main{
    background-color: rgb(33,45,58);
    height: 100%;
    .loader{
      height: 100vh;
    }
  }
</style>
