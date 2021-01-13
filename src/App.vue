<template>
  <div id="nav">
    <p class="logo">CSGO Gamble</p>
    <router-link to="/">Home</router-link> |
    <router-link to="/shop">Shop</router-link> |
    <router-link to="/about">Contact</router-link> |
    <router-link to="/cart"><img src="./views/cart.svg" class="cart"></router-link>
  </div>
  <router-view/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body{
  background-color: rgb(9, 12, 37);
}

#nav {
  padding: 30px;
  background-color: rgb(9, 12, 37);
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 0.1rem;
}

#nav a {
  font-weight: bold;
  color: #ffffff;
  padding: 10px;
  width: 90px;
  text-decoration: none;
}

#nav a.router-link-exact-active {
  color: #ffffff;
  background-color: rgb(223, 60, 46);
  border-radius: 5px;
}

.logo{
  color: white;
  font-size: 20px;
}

.cart{
  width: 1.2rem;
  height: 1.2rem;
}
</style>
