<template>
<h1 class="msg">You're on your way to wasting your money</h1>
<div class="pageDiv">
    <div class="itemDiv">
        <img :src="src" class="img">
        <div class="itemDesc">
            <p class="name">{{name}}</p>
            <p class="price">$ {{price}}</p>
            <p class="desc">{{desc}}</p>
            <router-link :to="{ name: 'Cart', params: {id: id, name: name, desc: desc, src: src, price: price}}"><button class="buyBtn">Buy Now</button></router-link>
            
        </div>
    </div>
</div>
</template>

<script>
export default {
    props: ['id', 'name', 'desc', 'src', 'price'],
    data(){
        return{
            id: this.$route.params.id,
            title: this.$route.params.title
        }
    }
}
</script>

<style>
.itemDiv{
    display: flex;
    align-items: center;
    flex-direction: row;
    justify-content: center;

    width: 50rem;
}
.itemDesc{
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;

}
.name{
    color: white;
    font-size: 2rem;
}
.desc{
    color: rgba(255, 255, 255, 0.705);
    font-size: 1rem;
}
.pageDiv{
    display: flex;
    align-items: center;
    justify-content: center;
    transform: scale(1.5);
    margin-top: 8rem;
}
.buyBtn{
    background-color: rgb(223, 60, 46);
    color: white;
    padding: 15px;
    border: none;
    outline: none;
    border-radius: 5px;
    cursor: pointer;
}
.buyBtn:hover{
   background-color: rgb(204, 56, 43); 
}
.msg{
    margin-top: 3rem;
}
.price{
    color: rgb(255, 255, 255);
    font-size: 1.3rem;
}
</style>