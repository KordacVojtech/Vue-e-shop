<template>
  <div class="purchaseDiv">
      <h1 class="thanks">Thank you for your purchase!</h1>
      <p v-for="item in items">{{item}}</p>
      <router-link :to="{name: 'Shop'}">
        <button class="buyBtn">Return to Shop</button>
      </router-link>
      
  </div>
</template>

<script>
export default {
  props: ['items']
}
</script>

<style>
.purchaseDiv{
  margin-top: 10rem;
}
.thanks{
  color: white;
}
</style>