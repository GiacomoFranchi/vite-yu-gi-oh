<script>
export default {
    
}
</script>
<template>
<select  aria-label="Default select example">
    <option selected>Alien   </option>
    <option value="1">One</option>
    <option value="2">Two</option>
    <option value="3">Three</option>
</select>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;

select{
    font-size: 1rem;
    padding: 1rem 0.8rem;
    border: none;
    border-radius: 15px;
    margin: 1rem 0 1rem  10%;
    font-size: 1.5rem;
}
</style>