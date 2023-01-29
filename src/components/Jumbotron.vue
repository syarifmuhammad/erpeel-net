<template>
    <div class="w-full mb-10 mt-[73px]">
        <div class="md:max-w-[1024px] mx-auto">
            <div class="w-full h-[500px] rounded-bl-[100px] flex items-center bg-cover bg-right"
                :style="{ backgroundImage: `url(${tabletImage})` }">
                <div class="w-[80%] mx-auto mt-[-30px] flex flex-col justify-center items-center md:block">
                    <!-- <div> -->
                    <h1 class="text-4xl text-[#10a6a5] mb-3">ERPEEL.NET</h1>
                    <p class="text-xl text-[#10a6a5] mb-12">Solusi Internet Rumah Anda</p>
                    <button class="bg-white px-8 py-2 text-[#10a6a5] rounded-3xl">Info Selengkapnya</button>
                    <!-- </div> -->
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import tabletImage from '../assets/tablet.jpg'
export default {
    name: "Jumbotron",
    data() {
        return {
            tabletImage: tabletImage,
        }
    }
}
</script>
<style scoped>
* {
    font-family: "TelkomselBatikSans-Bold", Helvetica, Arial;
}
</style>