<template>
  <div class="v-main-wrapper">
    <transition>
      <keep-alive>
    <router-view></router-view>
      </keep-alive></transition>
    <p>{{title}}</p>
    <p>In this adorable online store, you can purchase unusual living creatures.</p>
    <p>Plunge headlong into the world of fairy tales and magic.</p>
    <p>Let yourself be unique by having a mystical friend from our store.</p>
<!--   <v-catalog />-->
<!--    <v-cart-->
<!--        v-if="CART.length"-->
<!--        :cart_data="CART"-->
<!--    />-->
  </div>
</template>

<script>
  // import vCatalog from './v-catalog'
  // import vCart from './v-cart'

 export default {
   name: "v-main-wrapper",
   // components:{
   //   vCatalog,
   //   vCart
   // },
   props:{},
   data(){
     return{
       title: 'ONLINE-SHOP OF YOUR DREAMS',
     }
   },
   computed:{},
   methods: {},
   watch:{}
 }
</script>

<style>
 .v-main-wrapper{
   max-width: 900px;
   margin: 0 auto;
 }
</style>