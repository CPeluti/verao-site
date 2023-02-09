<template>
    <div>
        <div class="relative container overflow-hidden h-screen">
            <div class="text grid place-content-center gap-2">
            <h1 class="text-5xl leading-tight text-white"> First Summer<br/> School<br/> on<br/> Robotic<br/> Mission<br/> Engineering</h1>
            <div class="grid place-content-center gap-1">
                <span>
                <h3 class="text-white flex items-center justify-center gap-x-2">
                    <CalendarIcon class="w-6 h-6 inline"/>
                    02 Mar 2023 - 05 Mar 2023
                </h3>
                </span>
                <span>
                <h3 class="text-white flex items-center justify-center gap-x-2">
                    <MapPinIcon class="w-6 h-6 inline"/>
                    <span class="text-start">
                    Departamendo de ciência da computação, UnB
                    </span>
                </h3>
                </span>
            </div>
            </div>
            <img id="cover" class="z-0 h-full w-full object-cover" src="@/assets/cic_unb.jpg"/>
        </div>
    </div>
</template>

<script setup lang="ts">
import {MapPinIcon, CalendarIcon} from '@heroicons/vue/24/solid' 
</script>

<style lang="scss" scoped>
.container{
  margin: -5px, -10px, -10px, -5px;
}
.text{
  @apply z-10 absolute w-full text-center top-1/2 left-1/2 leading-tight -translate-x-1/2 -translate-y-1/2
}
h1{
  font-family: 'roboto';
}
#cover{
  object-fit: cover;
  transform: scale(1.3);

  filter: blur(8px) brightness(60%);

}
</style>