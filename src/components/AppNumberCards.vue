<script>
import { store } from "../store";
export default {
  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div>
    <p>Found {{ store.cards.length }} cards</p>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

div{
    width: 90%;
    margin: 0  auto;
    background-color:$nCard-color;
    padding: 0.5rem 0.8rem;
    p{
        color: white;
        font-weight: bold;
    }
}
</style>