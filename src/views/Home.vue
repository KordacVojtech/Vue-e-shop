<template>
  <div class="home">
    <h1 class="titleHome">Buy the best skins <br><br> Waste your money</h1>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  components: {
  }
}
</script>

<style>
  .home{
    display: flex;
    align-items: center;
    justify-content: center;

    background: url('https://cdn1.dotesports.com/wp-content/uploads/2018/08/11124042/bded26c4-c2c4-48e7-b87f-c75fd2f339c3.jpg');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    min-height: 92vh;
  }

  .titleHome{
    color: rgb(223, 60, 46);
    text-shadow: 3px 3px 20px rgb(7, 27, 53);
    font-size: 5rem;
    min-height: 60vh;
  }
</style>