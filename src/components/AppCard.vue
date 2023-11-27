<script>
import { stringifyExpression } from '@vue/compiler-core';

export default {
  props: {
    character: Object,
  },
};
</script>

<template>
    <div v-for="data in character">
        <img v-for="image in data.card_images" :src="image.image_url" alt="" />
        <h3>{{ data.name }}</h3>
        <p>{{ data.archetype }}</p>
    </div>
  </template>
  
<style lang="scss" scoped>
@use "../style/partials/variables" as *;

div{
    width:calc(100% / 5 - 2rem);
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