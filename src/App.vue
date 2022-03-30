<template>
  <div id="app">
    <Header />
    <CardList />
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
  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap";

</style>
