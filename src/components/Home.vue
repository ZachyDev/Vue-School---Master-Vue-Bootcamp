<template>
  <div>
      <h1 @click="sayHello">This is Zachy - #TIZ😄</h1>
  </div>
</template>

<script>
export default {
    name: "Home",
    components: {},
    methods: {
        sayHello() {
            alert('hello')
        }
    }
}
</script>

<style>

</style>