<template>
    <div class="container-fluid">
        <div class="row py-5">
            <div class="col-lg-6">
            <nuxt-link to="/pengunjung/tambah">
                <div class="card bg-pengunjung rounded-5">
                    <div class="card-body">
                        <h2  class="text-light">pengunjung</h2>
                    </div>
                </div>
            </nuxt-link>
            </div>

            <div class="col-lg-6">
                <nuxt-link to="/buku">
                <div class="card bg-buku rounded-5">
                    <div class="card-body">
                        <h2  class="text-light">cari buku</h2>
                    </div>
                </div>
                </nuxt-link>
            </div>
        </div>
        <h2>Statistik</h2>
        <div class="row py-5">
            <nuxt-link to="/pengunjung/index"></nuxt-link>
            <div class="col-lg-6">
                <nuxt-link to="/pengunjung">
                <div class="card pengunjung rounded-5">
                    <div class="card-body">
                        <h1 class="text-center" style="margin-top: 80px;"> {{ jmlpengunjung }} pengunjung</h1>
                    </div>
                </div>
                </nuxt-link>
            </div>

            <div class="col-lg-6">
                <nuxt-link to="/buku">
                <div class="card buku rounded-5">
                    <div class="card-body">
                        <h1 class="text-center" style="margin-top: 80px;">{{ jmlbooks }} buku</h1>
                    </div>
                </div>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container-fluid {
    /* padding: 0;
    margin: 0; */
    background-image: url('../assets/img/bg-cr-bk.jpg');
}
.card {
    height: 250px;
    box-shadow: 1px 1px 10px hsl(0, 0%, 100%)
}
.card.bg-pengunjung {
    background-image: url('../assets/img/bg-bk-knj.jpeg');
    background-repeat: no-repeat;
    background-position: center center;
    background-size: cover;
}
.card.bg-buku {
    background: url('../assets/img/bg-cr-bk.jpg') no-repeat center center;
    background-size: cover;
}

.pengunjung {
    background-color: #EAC029;
}
.buku {
    background-color: #EAC029;
}

</style>

<script setup>
const supabase= useSupabaseClient()

const keyword = ref('')
const visitors = ref([])
const jmlpengunjung= ref(0)
const jmlbooks= ref(0)

const getPengunjung =async () => {
  const { data, error } = await supabase
  .from('pengunjung')
  .select(`*, keanggotaan(*), keperluan(*)`)
  .ilike("nama",`%${keyword.value}%`)
  .order('tanggal', { ascending: false})
  if(data) visitors.value = data
}

const getJmlPengunjung = async () => {
  const{ data, count } = await supabase
    .from("pengunjung") 
    .select('*', { count: "exact" })
    if(data) jmlpengunjung.value = count
}

const getJmlBooks = async () => {
  const{ data, count } = await supabase
    .from("buku") 
    .select('*', { count: "exact" })
    if(data) jmlbooks.value = count
}

onMounted(() =>{
  getPengunjung()
  getJmlPengunjung()
  getJmlBooks()
})

</script>
