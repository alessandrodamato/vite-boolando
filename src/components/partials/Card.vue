<script>
  export default {
    props:{
      card: Object
    },

    methods:{
      getPathImage(img){
        return new URL(`../../assets/img/${img}`, import.meta.url).href
      },

      discountCalc(){
        let p = this.card.price;
        let d;
        let lowerPrice;

        this.card.badges.forEach(badge => {
          if (badge.type === 'discount') {
            d = -parseInt(badge.value);
          } else {
            d = 0
          }
        });

        lowerPrice = this.card.lowerPrice = p - (p * d) / 100;
        return lowerPrice.toFixed(2)

      }
    }
  }
</script>

<template>
  
  <div class="product">

    <div class="product-img">
      <img class="main-img" :src="getPathImage(card.frontImage)" :alt="card.brand">
      <img class="hover-img" :src="getPathImage(card.backImage)" :alt="card.brand">
      <div class="f-size-small tags">
        <!-- ciclo i badge al contrario (per rispecchiare boolando originale) -->
        <div
          v-for="(badge, index) in card.badges.slice().reverse()"
          :key="index"
          class="badge"
          :class="badge.type"
        >
        {{badge.value}}
        </div>
      </div>
      <div
        class="favourite"
        :class="{'active' : card.isInFavorites === true}"
        @click="card.isInFavorites = !card.isInFavorites"
        >&hearts;
      </div>
    </div>

    <div class="f-size-small product-brand">{{ card.brand }}</div>

    <div class="product-name">{{ card.name }}</div>

    <span class="f-size-small lower-price">{{ discountCalc() }} &euro;</span>
    
    <span class="f-size-small price">{{ card.price }} &euro;</span>

  </div>

</template>

<style lang="scss" scoped>

@use '../scss/partial/variables' as *;

.product{
  margin: 50px 10px 0;
  .product-img{
    position: relative;
    cursor: pointer;
    img{
      width: 400px;
    }
    .hover-img, &:hover .main-img{
      display: none;
    }
    &:hover .hover-img{
      display: inline-block;
    }
    .tags{
      position: absolute;
      bottom: 40px;
      left: 0;
      .badge{
        display: inline-block;
        padding: 5px;
        font-weight: bold;
        color: white;
      }
      .discount{
        background-color: $color-discount;
      }
      .tag{
        background-color: $color-eco;
      }
    }
    .favourite{
      position: absolute;
      top: 10px;
      right: 0;
      padding: 8px 15px;
      font-size: 2rem;
      background-color: white;
      &.active{
        color: $color-primary;
      }
    }
  }
  .product-name{
    font-weight: bold;
    text-transform: uppercase;
  }
  .lower-price{
    font-weight: 900;
    color: $color-discount;
  }
  .price{
    text-decoration: line-through;
  }
}

</style>