<template>
  <div class="app">
    <div class="header">
      <button v-if="state==='default'" class="btn btn-primary" @click="changeState('edit')" style="margin-top:30px;">Add Item</button>
      <button v-else class="btn btn-danger" @click="changeState('default')" style="margin-top:30px;">Cancel</button>
    </div>
    <div v-if="state==='edit'">
      <input type="text" v-model="newItem" placeholder="Add to cart" @keyup.enter="addToCart">
      <button type="button" class="btn btn-primary" @click="addToCart" :disabled="newItem.length === 0">Save Item</button>
      <button class="btn btn-success" @click="showItems" style="margin-top:20px;">Show List</button>
    </div>
    <ShopStore :shoplists="shoplists"/>
    <a :href="newItem" target="_blank">Dynamic Link</a>
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
      state: 'default',
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
    },
    changeState(newState) {
      this.state = newState;
      this.newItem = '';
    }
  }
}
</script>

<style scoped>
  .app{
    background: #444;
    width: 100%;
    height: 100vh;
    max-width: 100%;
    position: absolute;
    margin-top: -10px;
  }
  .app input[type="text"] {
    display: flex;
    width: 250px;
    height: 30px;
    margin:30px auto;
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
  .app p {
    position: absolute;
    left: 600px;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 20px;
    color: #fff;

  }
</style>