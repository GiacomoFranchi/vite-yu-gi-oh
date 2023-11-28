<script>
import axios from "axios";
import AppHeader from "./components/AppHeader.vue";
import AppMain from "./components/AppMain.vue";
import { store } from "./store.js";


export default {
  data() {
    return {
      store,
    };
  },
  created() {
    this.store.loading = true;
    axios.get(this.store.apiUrl).then((resp) => {
      this.store.cards = resp.data.data;
      this.store.loading = false;
    });
  },
  components: { AppHeader, AppMain },
};
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style lang="scss">
@use "./style/general.scss"

</style>
