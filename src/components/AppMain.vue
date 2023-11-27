<script>
import AppCardList from './AppCardList.vue';
import selectButton from './selectButton.vue';


export default {
    components:{
    selectButton,
    AppCardList
}    
}
</script>

<template>
    <main>
        <selectButton />
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
    