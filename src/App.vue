<template>
<div class="container">
  <app-header></app-header>
  <div class="row">
    <div class="col-md-12">
      <router-view></router-view>
    </div>
  </div>
</div>
</template>

<script>
import Header from './components/Header.vue'
export default {
  components: {
    'appHeader': Header
  },
  created() {
    this.$store.dispatch('initStocks');
  }
}
</script>

<style>
  body {
    background-color: #366635;
    padding: 20px;
  }
</style>
