<script>
import { store } from "../store";
import AppCard from "./AppCard.vue";


export default {
  data() {
    return {
      store,
    };
  },
  components: { AppCard, },
};
</script>

<template>
    <div class="container">
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
        gap: 15px;
        flex-wrap: wrap;
        justify-content: space-between;        
        .col{
            width: calc(100% / 5 - 30px); 
        }
    }
 }
</style>