<template>
  <div class="app">
    <input type="text" v-model="addToCart" placeholder="Add to cart">
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
      addToCart: '',
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
    background: #444;
    width: 100%;
    height: 70vh;
    max-width: 100%;
    position: absolute;
    margin-top: -10px;
  }
  .app input[type="text"] {
    display: flex;
    width: 250px;
    height: 30px;
    margin:15px auto;
    outline: none;
    border:none;
    border-radius: 7px;
  }
</style>