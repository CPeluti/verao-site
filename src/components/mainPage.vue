<template>
    <div class="snap-mandatory snap-y">
        <div id="start" class="snap-center relative container overflow-hidden h-screen">
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
        <div class="snap-center p-10 grid gap-10">
          <div>
            <h2>Description</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa optio architecto totam voluptate laborum expedita tempora quod voluptatibus sed numquam, eligendi alias dolorum animi aut fugit in quas, necessitatibus exercitationem.</p>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Rem animi aspernatur et iure est maiores suscipit optio quaerat nobis molestias. Recusandae beatae sapiente sunt vitae ab nemo accusamus, quis soluta?</p>
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut, placeat adipisci maxime fuga reprehenderit culpa soluta voluptate temporibus mollitia tempora voluptates rem molestiae vel similique, fugit rerum suscipit. Recusandae, voluptate.</p>
          </div>
          <div>
            <h2>Place</h2>
            <div class="google-maps">
              <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d479.9817788114817!2d-47.86940130027329!3d-15.758848781485668!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x935a3bb88f71361f%3A0x3933d293e644ad55!2zUHLDqWRpbyBkZSBDacOqbmNpYSBkYSBDb21wdXRhw6fDo28gZSBFc3RhdMOtc3RpY2EgLSBDSUMvRVNU!5e0!3m2!1spt-BR!2sbr!4v1676040838810!5m2!1spt-BR!2sbr" style="border:0;" allowfullscreen="false" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
          </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import {MapPinIcon, CalendarIcon} from '@heroicons/vue/24/solid' 
</script>

<style lang="scss" scoped>
.google-maps {
    position: relative;
    padding-bottom: 75%; // This is the aspect ratio
    height: 0;
    overflow: hidden;
}
.google-maps iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100% !important;
    height: 100% !important;
}
.container{
  margin: -5px, -10px, -10px, -5px;
}
.text{
  @apply z-10 absolute w-full text-center top-1/2 left-1/2 leading-tight -translate-x-1/2 -translate-y-1/2
}
h1{
  font-family: 'roboto';
}
h2{
  font-family: 'roboto';
  @apply text-black font-bold text-2xl mb-2
}
p{
  font-family: 'roboto';
  @apply text-black text-lg
}
#cover{
  object-fit: cover;
  transform: scale(1.3);

  filter: blur(8px) brightness(60%);

}
</style>