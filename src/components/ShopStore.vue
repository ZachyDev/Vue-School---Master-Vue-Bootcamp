<template>
  <div class="shoplist">
      <h1>Shoprite - Shop with us!</h1>
      <div :key="shoplist" v-for="shoplist in shoplists">
        <ShopListItems :shoplist="shoplist"/>
      </div>
  </div>
</template>

<script>
import ShopListItems from './ShopListItems';
export default {
    name: "ShopStore",
    components: {
        ShopListItems
    },
    props: {
        shoplists: Array
    }
}
</script>

<style scoped>
    .shoplist {
        width: 80%;
    }
    .shoplist h1 {
        color: #fff;
        display: flex;
        justify-content: center;
        margin-top: 50px;
    }
    .shoplist input[type="text"] {
        border:none;
        padding: 10px;
        width: 500px;
        display: flex;
        margin-bottom:30px;
    }
</style>