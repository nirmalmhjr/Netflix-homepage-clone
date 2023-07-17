<template>
    <div class="w-[45%] pt-20">
        <div class="text-6xl font-semibold font-serif">{{ movie.movie.name }}</div>
        <div class="flex relative text-lg pt-4">
            <div class="text-lg">{{ movie.movie.year }}</div>
                <div class="relative">
                    <div class="text-[40px] absolute -top-[14px] left-[3px]">.</div>
                    <div class="pl-4">{{ movie.movie.genre.one }}</div>
                </div>
                <div class="relative">
                    <div class="absolute text-[40px] -top-[14px] left-[3px]">.</div>
                    <div class="pl-4">{{ movie.movie.genre.two }}</div>
                </div>
                <div class="relative">
                    <div class="absolute text-[40px] -top-[14px] left-[3px]">.</div>
                    <div class="pl-4">{{ movie.movie.genre.three }}</div>
                </div>
            </div>
        
        <div class="text-2xl pt-6">{{ movie.movie.description }}</div>
    </div>
</template>

<script setup>
 const movie= defineProps({
                    movie:Object
                })  

</script>