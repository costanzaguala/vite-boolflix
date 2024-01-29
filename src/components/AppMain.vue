<script>

import { store } from '../store.js';

export default {
    data() {
        return {
            store,
        };
     },
    methods: {
        getFlag(language) {
            let link = ''
            if (language == 'en') {
                link = 'https://flagicons.lipis.dev/flags/4x3/gb.svg';
            }
            else if (language == 'ja') {
                link = 'https://flagicons.lipis.dev/flags/4x3/jp.svg';
            }
            else {
                link = 'https://flagicons.lipis.dev/flags/4x3/' + language + '.png';
            }

            

            return link;
        }
    }
}
</script>

<template>
    <main>
         <div>
            <h2>
                Movies
            </h2>
            <ul>
                <li v-for="(movie,i) in store.movies" :key="i">
                    
                    <div>
                        Title: {{ movie.title }}
                    </div>
                    
                    <div>
                        Original Title: {{ movie.original_title }}
                    </div>

                    <div>
                        Original Title: {{ movie.original_language }}
                    </div>
                    
                    <div>
                        Flag:
                        <img :src="getFlag(movie.original_language)" :alt="movie.original_language">
                    </div>
                    
                    <div>
                        Vote average: {{ movie.vote_average }}                   
                    </div>

                </li>
            </ul>
         </div>

         <hr>

         <div>
            <h2>
                Series
            </h2>
            <ul>
                <li v-for="(singleSeries,i) in store.series" :key="i">
                    
                    <div>
                        Name: {{ singleSeries.name }}
                    </div>
                    
                    <div>
                        Original Name: {{ singleSeries.original_name }}
                    </div>

                    <div>
                        Original Language: {{ singleSeries.original_language }}
                    </div>
                    
                    <div>
                        Flag:
                        <img :src="getFlag(singleSeries.original_language)" :alt="singleSeries.original_language">
                    </div>
                    
                    <div>
                        Vote average: {{ singleSeries.vote_average }}                   
                    </div>

                </li>
            </ul>
         </div>
    </main>
</template>

<style lang="scss" scoped>
img {
    height: 30px;
}
</style>