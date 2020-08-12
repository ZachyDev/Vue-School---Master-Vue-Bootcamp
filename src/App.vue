<template>
  <div>
    <Home name="name"/>
  </div>
</template>

<script>
import Home from './components/Home';
export default {
  name: "App",
  components: {
    Home
  },
  data() {
    return {
      name: 'vue'
    }
  }
}
</script>

<style>

</style>