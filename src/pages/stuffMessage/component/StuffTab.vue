<template>
    <div class="stuff_tab">
      <button class="btn_buy" v-if="stuffDetailMessage.rentOrSail !== 1" @click="handleBuyClick">购买{{buy_price}}</button>
      <button class="btn_rent" v-show="stuffDetailMessage.rentOrSail !== 0" @click="handleRentClick">租赁{{rent_price}}</button>
    </div>
</template>

<script>
  import { mapActions, mapGetters } from "vuex";

  export default {
      name: "StuffTab",
      data() {
        return {
          buy_price: '230',
          rent_price: '20',
          rent: '',
          buy: ''
        };
      },
    computed: {
      ...mapGetters({
        stuffDetailMessage: "getStuffDetailMessage",
      }),
    },
    methods: {
      handleBuyClick() {
        console.log("handleBuyClick");
        this.$router.push({
          name: "BuyStuff",
          params: {
          }
        })
      },
      handleRentClick(){
        console.log("handleRentClick");
        this.$router.push({
          name: "RentStuff",
          params: {
          }
        })
      }
    }
    }
</script>

<style scoped>
  .stuff_tab{
    width: 100%;
    height: 10vh;
    display: flex;
    position: absolute;
    bottom: 0;
    justify-content: space-around;
    align-items: center;
    background-color: rgba(78,93,107,0.43);
    border-radius: 30px 0 0 0;
    /*background-color: #4e5d6b6e;*/
  }
  .btn_buy, .btn_rent{
    width: 35vw;
    height: 60%;
    /* display: flex; */
    /* justify-items: center; */
    border: none;
    border-radius: 32px;
  }
  .btn_buy{
    /*background-color: #335165;*/
    background-color: #899e92;
    color: aliceblue;
  }
  .stuff_tab button{

  }
</style>
