<template>
  <main>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <Card />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Card from './Card.vue'
export default {
  components: { Card },
  name: 'CardList',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  main{
    background-color: rgb(33,45,58);
    height: 90vh;
  }
</style>
