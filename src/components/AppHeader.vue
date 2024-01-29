<script>
import { store } from '../store.js';

export default {
    data() {
        return {
            store
             
        };
     },
  
} 
</script>

<template> 
    <header>
        <input v-model="store.searchInput" type="text" name="" placeholder="Inserisci il nome di un film...">
        <button @click="$emit('performSearch')">
            Cerca
        </button>
    </header> 
</template>

<style lang="scss" scoped>

</style>
