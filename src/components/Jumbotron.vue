<script>
export default {
    setup() {
        function getImageUrl(name) {
            return new URL(`/src/assets/${name}`, import.meta.url).href
        }

        return {
            getImageUrl,
        }
    }
}
</script>

<template>
    <div class="w-full mb-10 mt-[73px]">
        <div class="md:max-w-[1024px] mx-auto">
            <div
                class="w-full h-[500px] rounded-bl-[100px] flex items-center bg-cover bg-right bg-[url('tablet.jpg')]">
                <div class="w-[80%] mx-auto mt-[-30px]">
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
<style scoped>
* {
    font-family: "TelkomselBatikSans-Bold", Helvetica, Arial;
}
</style>