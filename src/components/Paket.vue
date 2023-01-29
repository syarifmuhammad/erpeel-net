<template>
    <div class="w-full py-10" id="harga">
        <div class="lg:max-w-[1024px] md:max-w-[768px] px-4 md:px-0 mx-auto">
            <h1 class="text-4xl mb-10">Pilihan Paket Voucher</h1>
            <div class="grid-cols-1 sm:grid-cols-2 md:grid-cols-3 grid gap-4">
                <div class="card p-5 rounded-xl text-white" v-for="data in packaged">
                    <div class="flex items-center mb-2">
                        <img class="w-[25px] rounded-full mr-3" src="../assets/logovoucher.jpg" />
                        <h2 class="text-xl">{{ data.name }}</h2>
                    </div>
                    <h3 class="text-2xl mb-2">{{ toRupiah(data.price) }}</h3>
                    <p class="text-sm font-thin mb-4">
                        {{ data.description }}
                    </p>
                    <a target="_blank" href="https://api.whatsapp.com/send?phone=6281232843422&text=Saya%20ingin%20Beli%20Voucher%20internet%20" class="cursor-pointer px-6 py-2 bg-white text-[#10a6a5] rounded-3xl text-sm">Beli paket</a>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { createClient } from '@supabase/supabase-js'
export default {
    name: 'Paket',
    data() {
        return {
            packaged: []
        }
    },
    async created() {
        const supabaseUrl = 'https://ghtsccdtlmslnbyaiqmt.supabase.co'
        const supabaseKey = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImdodHNjY2R0bG1zbG5ieWFpcW10Iiwicm9sZSI6ImFub24iLCJpYXQiOjE2NzQ5NjQ0ODEsImV4cCI6MTk5MDU0MDQ4MX0.3HMLqMHZvL5t0FVMC6a_Q1CnPZAkBXfxYsfysDvNzCk'
        const supabase = createClient(supabaseUrl, supabaseKey)
        const { data } = await supabase.from('package').select()
        console.log(data)
        this.packaged = data
    },
    methods: {
        toRupiah(nStr) {
            nStr += '';
            var x = nStr.split('.');
            var x1 = x[0];
            var x2 = x.length > 1 ? '.' + x[1] : '';
            var rgx = /(\d+)(\d{3})/;
            while (rgx.test(x1)) {
                x1 = x1.replace(rgx, '$1' + '.' + '$2');
            }
            return x1 + x2;
        }
    }
}
</script>
<style scoped>
* {
    font-family: "TelkomselBatikSans-Bold", Helvetica, Arial;
}

p {
    font-family: Arial, Helvetica, sans-serif;
}

.card {
    background: url("/pbg.png"), linear-gradient(165deg, #00c5b3 0%, rgba(85, 101, 105) 100%);
}
</style>