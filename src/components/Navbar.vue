<template>
    <header class="bg-white fixed left-0 top-0 w-full">
        <div class="flex justify-between content-center py-3 lg:max-w-[1024px] md:max-w-[768px] px-4 md:px-0 mx-auto">
            <div class="logo flex justify-center content-center">
                <a href="/">
                    <img class="w-[50px] h-[50px]" :src="getImageUrl('wfi.png')" />
                </a>
                <!-- <input class="menu-btn" type="checkbox" id="menu-btn" /> -->
                <label class="menu-icon" for="menu-btn"><span class="navicon"></span></label>
            </div>
            <ul class="gap-10 items-center justify-between hidden md:flex">
                <li><a class="menu-link" href="">Home</a></li>
                <li><a class="menu-link" href="#fitur">Fitur</a></li>
                <li><a class="menu-link" href="#harga">Harga</a></li>
                <!-- <li><a class="menu-link" href="bantuan.html">Bantuan</a></li> -->
                <li><a class="menu-link" href="#kontak">Kontak</a></li>
            </ul>
        </div>
    </header>
</template>
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
<style>
.menu-link {
    font-family: "TelkomselBatikSans-Bold", Helvetica, Arial;
    transition: .2s;
}

.menu-link:hover {
    color: #10a6a5;
}

</style>