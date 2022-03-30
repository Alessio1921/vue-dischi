<template>
  <div>
    <div class="card my-2 ">
      <img :src="card.poster" class="card-img-top p-3 pb-0" alt="...">
      <div class="card-body text-center pt-0">
        <h5 class="card-title text-white">{{card.title}}</h5>
        <p class="card-text">{{card.author}}</p>
        <p class="card-text">{{card.year}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'homeCard',
  props:{'card': Object}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .card{
    height: 290px;
    width: 166px;
    border-radius: 0;
    background-color: rgb(48,58,69);
    img{
      height: 150px;
    }
    p{
      margin: 0;
      color: rgb(103,112,119);
    }
  }
</style>
