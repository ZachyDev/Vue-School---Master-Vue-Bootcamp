<template>
  <div class="app">
    <ShopStore :shoplists="shoplists"/>
  </div>
</template>

<script>
import ShopStore from './components/ShopStore'
export default {
  name: "App",
  components: {
    ShopStore
  },
  data() {
    return {
      shoplists: [
        
        { 
          id: 1,
          name: 'Laptop',
          price: 30000,
          dealer: 'Techfy'
        },
        {
          id: 2,
          name: 'Laptop',
          price: 30000,
          dealer: 'Techfy'
        },
        {
          id: 3,
          name: 'Laptop',
          price: 30000,
          dealer: 'Techfy'
        },
        {
          id: 4,
          name: 'Laptop',
          price: 30000,
          dealer: 'Techfy'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .app{
    background-color: #444;
    width: 100%;
    height: 50vh;
    display: flex;
    justify-content: center;
  }
</style>