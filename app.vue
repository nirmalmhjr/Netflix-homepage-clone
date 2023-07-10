<template>
  <div >
    <div class=" text-white bg-black w-full h-[100vh]">
      <div id="sideNav" class=" bg-white w-28 relative">
        <div  class="flex item-center">
          <img src="./public/images/netflix-logo.png" alt="" class="h-[70px] w-[50px] ">

          <Icon name="mdi:television" color="black" size="40"/>
        </div>
        <div id="sideNav">
          <Home fillColor="white" size="40"/>
        </div>
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