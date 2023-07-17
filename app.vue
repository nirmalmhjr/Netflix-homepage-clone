<template>
  <div >
    <div  class=" text-white bg-black w-full h-screen">
      <div v-if="!showFullVideo" id="sideNav" class=" w-[120px] relative flex item-center">
          <img src="images/netflix-logo.png" alt="" class=" w-[35px] absolute top-0  mt-5 ml-10">
     <div>
          <div class="py-2 px-10 mt-28">
            <Icon name="mdi:magnify" color="white" size="40"/>
          </div>
          <div class="py-2 px-10 my-6">
            <Icon name="mdi:home-outline" color="white" size="40"/>
          </div>
          <div class="py-2 px-10 my-6">
            <Icon name="mdi:trending-up" color="white" size="40"/>
          </div>
          <div class="py-2 px-10 my-6">
            <Icon name="mdi:television" color="white" size="40"/>
          </div>
          <div class="py-2 px-10 my-6">
            <Icon name="mdi:movie-outline" color="white" size="40"/>
          </div>
          <div class="py-2 px-10 my-6">
            <Icon name="mdi:plus" color="white" size="40"/>
          </div>
        </div>
      </div>

      <div v-if="!showFullVideo" class="fixed top-0 w-full h-[50%] pl-[120px] flex items-center">
        
        <MovieDetails v-if="movie" :movie="movie" class="z-40"/>

        <video
          v-if="movie"
          :src="`/videos/${movie.name}.mp4`"
          autoplay
          loop
          class=" h-[600px] absolute right-0 top-0"
        />
      </div>

        <div class="fixed bottom-0 right-0 w-full h-[55%] pl-[120px] overflow-y-auto ">
         
            <VideoCarousel :movies="movies[0]" category="Popular movies " class="pt-14 pb-14"
            start="0" />
            <VideoCarousel :movies="movies[1]" category="Featured movies" class="pt-14 pb-14" />
         
          <VideoCarousel :movies="movies[2]" category="Drama movies"/>
        </div>
    </div>
  </div>
</template>

<script setup>
import { storeToRefs } from "pinia";
import {useMovieStore} from './stores/movie'
import movies from './data/movies.json'

const useMovie = useMovieStore()

  const {movie, showFullVideo} = storeToRefs(useMovie)

  onMounted(()=> movie.value = movies[0][0])
</script>