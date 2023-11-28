<script>
import { store } from '../store';
export default {
    data(){
        return{
            store,
            options: [
                { text: '--', },
                { text: 'Alien', value: 'Alien' },
                { text: 'Ally of Justice', value: 'Ally of Justice' },
                { text: 'Ancient Gear', value: 'Ancient Gear' }
            ]
        }
    }
}
</script>

<template>
    <select @change="$emit('selChange')" v-model="store.selected">
        <option v-for="option in options" :value="option.value">
            {{ option.text }}
        </option>
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