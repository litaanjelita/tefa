<template>
    <div class="container-fluid">
        <div class="row content">
            <div class="col-lg-12">       
                <h2 class="text-center my-4">RIWAYAT PENGUNJUNG</h2>
                <nuxt-link to="/">
                    <button type="button" class="btn btn-warning mt-4 btn-lg">KEMBALI</button></nuxt-link>
            </div>
            <form @submit.prevent="getPengunjung">
                <div class="row my-3 d-flex justify-content-center">
                    <input v-model="keyword" type="search" class="col-lg-10 form-control- form-control-lg rounded-5" placeholder="Search..." style="background-color: #EAC029;">
                </div>
            </form>
                <div class="my-3 text-muted"></div>
                <table class="table table-bordered">
                    <thead>
                        <tr>
                            <td>NO</td>
                            <td>NAMA</td>
                            <td>KATEGORI</td>
                            <td>WAKTU/TANGGAL</td>
                            <td>KEPERLUAN</td>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="(visitor,i) in visitorFiltered" :key="i">
                            <td>{{ i+1 }}.</td>
                            <td>{{ visitor.nama }}</td>
                            <td>{{ visitor.keanggotaan.nama }}</td>
                            <td>{{ visitor.tanggal }}, {{ visitor.waktu }}</td>
                            <td>{{ visitor.keperluan.nama }}</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    
</template>

<script setup>
const supabase = useSupabaseClient()
const keyword = ref('')
const visitors = ref([])

const getPengunjung = async () => {
    const { data, error } = await supabase.from('pengunjung').select(`*, keanggotaan(*), keperluan(*)`)
    .ilike('nama', `%${keyword.value}%`)
    if(data) visitors.value = data
    visitors.value = data
}

const visitorFiltered = computed(() => {
    return visitors.value.filter((b) => {
        return (
            b.nama?.toLowerCase().includes(keyword.value?.toLowerCase())
        )
    })
})

onMounted(() =>{
    getPengunjung()
})
</script>


<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Irish+Grover&display=swap');
.container-fluid {
    background: url("../../assets/img/bg-cr-bk.jpg");
    background-size: cover;
    width: 100%;
}
td {
    color: white;
    border: 1px solid #fff;
    background-color: rgba(255, 255, 255, 0);
}

h2{
    color: white;
    font-family: "Irish Grover", system-ui;
}

.bi-caret-left-fill {
    margin-left: 20px;
}
</style> 
