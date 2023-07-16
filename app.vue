<template>
  <div >
    <div class=" text-white bg-black w-full h-screen">
      <div id="sideNav" class=" w-[120px] relative flex item-center">
          <img src="./public/images/netflix-logo.png" alt="" class=" w-[35px] absolute top-0  mt-5 ml-10">
      </div>
      
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
       

      <div>

        <MovieDetails />
      </div>

      <div>

        <VideoCarousel />
      </div>
    </div>
  </div>
</template>
<script setup>

</script>