<template>
    <div class="content">
        <div class="container py-5">
            <div class="row-mb-5">
                <div class="col">
                    <div class="card">
                        <h2 class="text-center mt-5">RINCIAN BUKU</h2>
                        <div class="container mt-5">
                            <div class="row">
                                <div class="col-3 p-5">
                                    <img class="img-fluid" src="@/assets/img/cover1.jpg" alt="" style="width:250px;">
                                </div>
                                <div class="col-8">
                                        <h4>KANCIL DAN RAJA HUTAN</h4>
                                        <h4>tahun terbit : 2013 </h4>
                                        <h4>penerbit : grasindo</h4>
                                        <h4>kategori : cerita anak</h4>
                                        <h4>deskripsi buku : cerita dari pulau jawa ini mengisahkan tentang kecerdikan seekor kancil  yang dengan tipu muslihatnya membuat seekor harimau menceburkan dirinya  ke dalam sebuah sumur yang dalam. Kancil melakukan hal ini karena  seluruh hewan yang berada di hutan ketakutan terhadap harimau yang  selalu memangsa mereka. </h4>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="row justify-content-end">
                <div class="col-1">
                    <nuxt-link to="/buku" class="row">
                        <button type="submit" class="btn justify-content-center btn-light btn-lg mr">BACK</button>
                    </nuxt-link>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
</script>

<style scoped>
.content{
    background-color: aquamarine;
}
.card{
    background-color: antiquewhite;
    border-radius: 25px;
}

</style>