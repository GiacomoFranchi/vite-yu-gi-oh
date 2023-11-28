<script>
import { stringifyExpression } from '@vue/compiler-core';

export default {
  props: {
    card: Object,
  },
};
</script>

<template>
    <div>
        <img :src="card.card_images[0].image_url" alt="" />
        <h3>{{ card.name }}</h3>
        <p>{{ card.archetype ? card.archetype : "Nessun Archetipo" }}</p>
    </div>
  </template>
  
<style lang="scss" scoped>
@use "../style/partials/variables" as *;

div{
    width:100%;
    height: 100%;
    margin: 1rem;
    text-align: center;
    background-color: $bg-color;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    img{
        width: 100%;
    }
    h3{
        font-size: 1.5rem;
        margin-bottom: 10px;
        color: white;
        font-weight: 300;
    }
    p{
        font-size: 1.2rem;
        
    }
}
</style>