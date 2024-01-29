<script>

import { store } from '../store.js';

export default {
    data() {
        return {
            store,
        };
     },
    methods: {

    }
}
</script>

<template>
    <main>
         <div>
            <ul>
                <li v-for="(movie,i) in store.movies" :key="i">
                    
                    <div>
                        Title: {{ movie.title }}
                    </div>
                    
                    <div>
                        Original Title: {{ movie.original_title }}
                    </div>

                    <div>
                        Original Language: {{ movie.original_language }}
                    </div>
                    
                    <div>
                        Vote average: {{ movie.vote_average }}                   
                    </div>

                    <hr>

                </li>
            </ul>
         </div>
    </main>
</template>

<style lang="scss" scoped>

</style>