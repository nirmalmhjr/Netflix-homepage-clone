<template>
    <div class="min-width-[1200px] relative">
        <div class="flex items-center font-semibold text-2xl cursor-pointer">
            {{ category }}
        </div>
       
     <v-slide-group
        center-active
        show-arrows
        max-items="1"
        class="-mx-4"
        >
        <v-slide-group-item
        v-for="(slide, index) in movies"
        :key="index"
        >
        <v-img
        aspect-ratio="1"
        width="150px" 
        height="200px"
            cover
            :src="`/images/${slide.name}.png`"
            class="mx-1"

        ></v-img>
      </v-slide-group-item>
    </v-slide-group>
    
    
    </div>
</template>

<script setup>
    import { storeToRefs } from 'pinia'
    import { useMovieStore } from '/stores/movie'
    import {Carousel, Slide, Navigation} from 'vue3-carousel'

    const useMovie = useMovieStore()
    const {movie, showFullVideo} = storeToRefs(useMovie) 

    const props = defineProps({
        movies: Array,
        category: String,
        start: String
    })
    const {category, movies, start} = toRefs(props)

    const currentSlide = ref(0)

    function fullScreenVideo(index){
        console.log('full screen',index);
    }

    function changeMovie(slide, index){
        movie.value = slide

        
      
    }
</script>

<style>
/* .v-carousel__controls{
  display: none;
} */
</style>