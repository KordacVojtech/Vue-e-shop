<template>
  <div class="cartDiv">
    <div>
      <img :src="src" class="img">
    </div>
    
    <div class="cartItems">
      <p style="color: white">{{name}}</p>
      <p class="price">$ {{price}}</p>
      <p>-------------------------</p>
      <div class="total">
        <p class="totalMsg">Total:</p>
        <p style="color: white">{{price}} USD</p>
      </div>
      <router-link :to="{ name: 'Purchase', params:{items: items}}">
      <button class="buyBtn" @click="addToCart">Pay Now</button>
      </router-link>

    </div>

  </div>
</template>

<script>
export default {
  name: 'Cart',
  props: ['id', 'name', 'desc', 'src', 'price', 'items'],
  data(){
    return{
      items: []
    }
  },
  methods:{
    addToCart(){
      this.items.push(this.name)
      console.log(this.items)
    }
  }
}
</script>

<style>
.cartItems{
  display: flex;
  align-items: flex-end;
  flex-direction: column;
  justify-content: center;
  
}
.cartDiv{
  display: flex;
  align-items: center;
  justify-content: center;
}
.total{
  display: flex;
  align-items: center;
}
.totalMsg{
  margin-right: 30px;
}
</style>