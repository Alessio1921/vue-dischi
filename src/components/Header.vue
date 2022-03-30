<template>
  <nav class="navbar">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img src="../assets/spotify.svg" alt="spotify logo" >
      </a>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'homeHeader',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  nav{
    background-color: rgb(48,58,69);
    height: 10vh;
    .container-fluid,a,img{
      height: 100%;
    }
  }
</style>
