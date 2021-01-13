<template>
  <div class="shop">
    <div v-for="item in items" :key="item.id" class="item">
      <router-link :to="{ name: 'SkinDetails', params: {id: item.id, name: item.name, desc: item.desc, src: item.src, price: item.price}}" class="itemLink"><img :src="item.src" class="img"></router-link>
      <router-link :to="{ name: 'SkinDetails', params: {id: item.id, name: item.name, desc: item.desc, src: item.src, price: item.price}}" class="itemLink">{{item.name}}</router-link>
    </div>
      
  </div>
</template>

<script>
let img1 = require('./imgs/skin1.png')

export default {
  name: 'Shop',
  data(){
    return{

      img: 'https://steamcdn-a.akamaihd.net/apps/730/icons/econ/default_generated/weapon_m4a1_silencer_cu_m4a1s_printstream_light_large.99e340c2eed00b54eef5320fd63e009fcede6cae.png',
      items: [
        {
          name: 'M4A1-S Printstream', 
          src: 'https://steamcdn-a.akamaihd.net/apps/730/icons/econ/default_generated/weapon_m4a1_silencer_cu_m4a1s_printstream_light_large.99e340c2eed00b54eef5320fd63e009fcede6cae.png',
          id: 1,
          price: 79.99,
          desc: 'From green to purple'
        },
        {
          name: 'Glock-18 Neo-Noir', 
          src: 'https://steamcdn-a.akamaihd.net/apps/730/icons/econ/default_generated/weapon_glock_cu_glock_noir_light_large.c93d0cbfa767d1f822a53ebfca0d57f532088c48.png',
          id: 2,
          price: 49.99,
          desc: 'Neo-Noir pea shooter'
        },
        {
          name: 'Five-SeveN | Fairy Tale', 
          src: 'https://steamcdn-a.akamaihd.net/apps/730/icons/econ/default_generated/weapon_fiveseven_cu_five_seven_diary_light_large.e09a26df236581e02db30cdbb9c55adb2a4d2292.png',
          id: 3,
          price: 9.99,
          desc: 'Got this from a case, nice'
        },
        {
          name: 'M4A4 | Cyber Security', 
          src: 'https://steamcdn-a.akamaihd.net/apps/730/icons/econ/default_generated/weapon_m4a1_cu_m4a4_cyberpunk_light_large.8ed70290de88498fcfdc0c89f23ba2ad60bd13a5.png',
          id: 4,
          price: 19.99,
          desc: 'SJW gun'
        },
        {
          name: 'AK-47 | Asiimov', 
          src: 'https://steamcdn-a.akamaihd.net/apps/730/icons/econ/default_generated/weapon_ak47_cu_ak47_asiimov_light_large.665fc3b83c8046398787a57d2ef7a9d938244820.png',
          id: 5,
          price: 99.99,
          desc: 'Best skin in the game'
        },
        {
          name: 'AK-47 | Fire Serpent', 
          src: 'https://steamcdn-a.akamaihd.net/apps/730/icons/econ/default_generated/weapon_ak47_cu_fireserpent_ak47_bravo_light_large.9390e7fd091ea8a0434fd2143e0acf0d5d1bbc97.png',
          id: 6,
          price: 579.99,
          desc: 'Clout AK'
        }
      ]
    }
  },
  components: {
  }
}
</script>

<style>
  .shop{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
  }

  .img:hover{
    transform: scale(1.03);
    transition-duration: 300ms;
    cursor: pointer;
  }
  .title{
    color: white;
  }
  .item{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
  }
  .itemLink{
    text-decoration: none;
    color: white;
    font-size: 1.5rem;
  }
</style>