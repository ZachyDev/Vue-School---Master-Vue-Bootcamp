<template>
  <div class="list-items"> 
      <ul>
          <li> {{ shoplist.dealer }}</li>
      </ul>
  </div>
</template>

<script>
export default {
    name: "ShopListItems",
    props: [ 'shoplist' ]
}
</script>

<style scoped>
    .list-items {
        border: 1px solid #bbb;
        width: 100%;
        display: flex;
        justify-content: start;
    }
    .list-items li {
        color: #fff;
        list-style-type: none;
        font-size: 18px;
        font-family: Arial, Helvetica, sans-serif;
    }

</style>