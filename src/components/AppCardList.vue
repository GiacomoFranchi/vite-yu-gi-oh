<script>
import { store } from "../store";
import AppCard from "./AppCard.vue";
import AppNumberCards from "./AppNumberCards.vue";


export default {
  data() {
    return {
      store,
    };
  },
  components: { AppCard, AppNumberCards },
};
</script>

<template>
    <div class="container">
        <AppNumberCards />
        <div class="row" >
            <div class="col" v-for="card in store.cards">
                <AppCard  :card="card" />
            </div>
        </div>
    </div>
</template>
  
<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.container{
    width: 90%;
    margin: 0 auto;
    padding: 2rem 0;
    .row{
        width: 100%;
        display: flex; 
        flex-wrap: wrap;
        justify-content: space-between;        
        .col{
            width: calc(100% / 5 - 20px); 
            margin: 10px;
        }
    }
 }
</style>