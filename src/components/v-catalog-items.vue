<template>
  <div class="v-catalog-items">
    <img class="v-catalog-items__images " :src="require('../assets/images/' + product_data.image)" alt="img">
    <p class="v-catalog-items__name">{{product_data.name}}</p>
    <p class="v-catalog-items__price">Price: {{product_data.price}} $</p>
    <button
        class="v-catalog-items__add_to_btn"
        @click="addToCart">
      Add to CART
    </button>
  </div>
</template>

<script>
 export default {
   name: 'v-catalog-items',
   props: {
     product_data:{
       type: Object,
       default() {
         return{}
       }
     }
   },
   data() {
     return{}
   },
   computed:{},
   methods: {
     addToCart() {
       this.$emit('addToCart', this.product_data);
     }
   },
   mounted() {
     this.$set(this.product_data, 'quantity', 1)
   }
 }
</script>

<style lang="scss">
  .v-catalog-items {
    flex-basis: 25%;
    box-shadow: 0 0 15px 0 #e0e0e0;
    padding: $padding*2;
    margin-bottom: $margin*2;
    &__images {
      width: 200px;
      height: 340px;
    }
  }
</style>