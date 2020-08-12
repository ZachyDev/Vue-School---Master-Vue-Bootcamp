<template>
  <div class="shoplist">
      <h1>Shoprite - Shop with us!</h1>
      <div :key="shoplist.id" v-for="shoplist in shoplists">
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
    .shoplist h1 {
        color: #fff;
    }
</style>