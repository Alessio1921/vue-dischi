<template>
  <main class="pb-5">
    <div class="container">
      <div class="row row-cols-3 row-cols-md-4 row-cols-lg-5 row-cols-xl-6">
        <div class="col" v-for="(element,index) in elementList" :key="index">
          <Card 
            :card="element"
          />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Card from './Card.vue'
import axios from 'axios'

export default {
  components: { Card },
  name: 'CardList',
  data:function(){
    return{
      elementList:null
    }
  },
  mounted() {
    axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(response => (this.elementList = response.data.response))
      .catch(error => {
        console.log(error)
      })
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  main{
    background-color: rgb(33,45,58);
    height: 100%;
  }
</style>
