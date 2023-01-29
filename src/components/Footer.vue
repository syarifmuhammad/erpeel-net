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
    <div class="w-full bg-[#10a6a5]" id="kontak">
        <div class="md:max-w-[1024px] mx-auto flex">
            <div class="w-1/3 flex flex-col content-center items-center border-r-2 py-10 pb-16">
                <img class="w-1/3 mb-3" src="../assets/logovoucher.jpg" alt="">
                <h6 class="text-white text-md">SURABAYA, JAWA TIMUR</h6>
                <p class="text-white text-sm mb-3">Internet Unlimited
                    Sepuasnya</p>
                <button class="px-6 py-2 bg-white text-[#10a6a5] text-sm rounded-sm">Whatsapp</button>
            </div>
            <div class="w-2/3 py-10 pb-16 px-10">
                <h2 class="text-4xl text-white">ERPEEL.NET</h2>
                <p class="text-sm text-white">Internet untuk warga</p>
                <hr class="my-8">
                <div class="flex items-center gap-4">
                    <img src="../assets/phone.png" class="w-[15px]" alt="">
                    <p class="text-white">0812-3284-3422</p>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>
* {
    font-family: "TelkomselBatikSans-Bold", Helvetica, Arial;
}

p {
    font-family: Arial, Helvetica, sans-serif;
}

.logoftr svg {
    fill: #10a6a5;
    text-align: center;
    width: 30%;
    margin: 10px auto;
}
</style>