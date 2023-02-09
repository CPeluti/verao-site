<template>
    <div :class="check ? basicClassHeader : classHeader">
        <h1 class="justify-self-start" :class="check?'text-white':'text-black'">
            RoME
        </h1>
        <div class="justify-self-end">
            <a :class="check ? basicButton : nonBasicButton" href="test">
                Participate
            </a>
        </div>
    </div>

</template>

<script setup lang="ts">
    import {ref, onMounted} from 'vue'
    const startScroll = ref(0)
    const check = ref(true)
    const basicClassHeader = "fixed px-6 pt-2 pb-1 grid w-screen grid-cols-2 justify-between items-center text-gray-900" 
    const basicButton = "rounded-lg px-4 w-26 h-7 py-1 bg-neutral-400 hover:bg-neutral-400 text-white bg-opacity-20 backdrop-blur-sm"
    const nonBasicButton = "rounded-lg px-4 w-26 h-7 py-1 bg-orange-300 text-black"
    const classHeader = "fixed px-6 pt-2 pb-1 grid w-screen grid-cols-2 justify-between items-center text-gray-900 bg-white" 
    const checkScroll = () => {
        if(startScroll.value >= window.scrollY){
            check.value = true
        } else {
            check.value = false
        }
    }
    onMounted(() => {
        // startScroll.value = window.scrollY
        window.addEventListener('scroll', checkScroll);
    })
</script>

<style lang="scss" scoped>
    a{
        font-family: 'roboto';
        font-size: 16px;
    }
    h1{
        font-family: 'Varela Round';
        font-size:24px;
    }
</style>