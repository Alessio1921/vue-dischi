<template>
  <nav class="navbar">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img src="../assets/spotify.svg" alt="spotify logo" >
      </a>
      <select class="form-select" v-model="selected" @change="selection(selected)">
        <option value="">Scegli un genere</option>
        <option value="Rock">Rock</option>
        <option value="Pop">Pop</option>
        <option value="Jazz">Jazz</option>
        <option value="Metal">Metal</option>
      </select>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'homeHeader',
  data:function(){
    return{
      selected:""
    }
  },
  methods:{
    selection(selected){
      console.log(selected);
      this.$emit('select', selected)
    }
  }
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
    select{
      width: 18%;
    }
  }
</style>
