<template>
  <div class="app">
    <input type="text" v-model="newItem" placeholder="Add to cart">
    <button type="button" class="btn btn-primary" @click="addToCart">Save Item</button>
    <button @click="showItems">Show List</button>
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
      newItem: '',
      shoplists: [
        
      ]
    }
  },
  methods: {
    addToCart() {
      this.newItem === '' ? alert('cart cannot be empty') : this.shoplists.push(this.newItem);  
    },
    showItems() {
      return this.shoplists.length > 0 ? alert(this.shoplists) : alert('Shopping cart is empty😔😔')
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
  .app button{
    display: flex;
    width: 100px;
    margin:0 auto;
    padding: 10px;
    outline: none;
    border-radius: 7px;
    cursor: pointer;
  }
</style>