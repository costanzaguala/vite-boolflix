<script>

import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';
import { store } from './store.js';


export default {
    data() {
        return {
            store,
             
        };
     },

    components: {
        AppHeader,
        AppMain,
    },

    methods: {
        search() {
            axios 
                .get('https://api.themoviedb.org/3/search/movie', {
                    params: {
                        api_key: 'c1fb2d9cb791b1a49d30ff785e40f309',
                        query: this.store.searchInput
                    }
                })

                .then((response) => {
                    console.log('Movies',response.data.results)
                    this.store.movies=response.data.results; 
                });
            
            axios 
                .get('https://api.themoviedb.org/3/search/tv', {
                    params: {
                        api_key: 'c1fb2d9cb791b1a49d30ff785e40f309',
                        query: this.store.searchInput
                    }
                })
                .then((response) => {
                    console.log('Series',response.data.results)
                    this.store.series=response.data.results; 
                });
        }
    }
}
</script>

<template> 

    <AppHeader @performSearch="search()"/>

    <AppMain/>

</template>

<style lang="scss">
    @use "assets/scss/main.scss" as *;
    @use "assets/scss/partials/reset.scss" as *;;
</style>
