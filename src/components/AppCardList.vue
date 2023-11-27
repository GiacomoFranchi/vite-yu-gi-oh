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
            <div class="col">
                <AppCard v-for="character in store.characters" :character="character" />
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
        .col{
            width: 100%;
            display: flex; 
            height: 100%;  
            flex-direction: row;
            flex-wrap: wrap;
            .AppCard{
                width: calc(100% / 5 - 0.5rem);
            }
        }
    }
 }
</style>