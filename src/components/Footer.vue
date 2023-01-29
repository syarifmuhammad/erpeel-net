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
        <div class="lg:max-w-[1024px] md:max-w-[768px] px-4 md:px-0 mx-auto flex flex-col items-center sm:flex-row">
            <div class="w-full sm:w-1/3 flex flex-col content-center items-center sm:border-r-2 py-10 pb-16">
                <img class="w-1/3 mb-3" src="../assets/logovoucher.jpg" alt="">
                <h6 class="text-white text-md text-center">SURABAYA, JAWA TIMUR</h6>
                <p class="text-white text-sm mb-3 text-center">Internet Unlimited
                    Sepuasnya</p>
                <button class="px-6 py-2 bg-white text-[#10a6a5] text-sm rounded-sm">Whatsapp</button>
            </div>
            <div class="w-full sm:w-2/3 py-10 pb-16 sm:px-10">
                <h2 class="text-4xl text-white text-center sm:text-start">ERPEEL.NET</h2>
                <p class="text-sm text-white text-center sm:text-start">Internet untuk warga</p>
                <hr class="my-8">
                <div class="flex items-center justify-center sm:justify-start gap-4">
                    <img src="../assets/phone.png" class="w-[15px]" alt="">
                    <p class="text-white text-center sm:text-start">0812-3284-3422</p>
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