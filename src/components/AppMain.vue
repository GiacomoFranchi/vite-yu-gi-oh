<script>
import { store } from "../store.js";
import AppCardList from './AppCardList.vue';
import selectButton from './selectButton.vue';
import axios from "axios";


export default {
    data(){
        return{
            store,
        };
    },
    components:{
    selectButton,
    AppCardList
    },
    methods:{
        selArchetype(){
            axios.get(this.store.apiUrl,{
                params:{
                    archetype: this.store.selected,
                },
            })
            .then((resp) => {
                this.store.cards = resp.data.data;
            });
            console.log("archetype")
        }
    },
}
</script>

<template>
    <main>
        <selectButton @selChange="selArchetype" />
        <div class="main-section">
            <AppCardList />
        </div>
    </main>
</template>
    
<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

main{
    width: 100%;
    background-color: $bg-color;
    padding: 0.5rem;
    .main-section{
        width: 90%;
        background-color: white;
        margin: 0 auto;
    }
}
</style>
    