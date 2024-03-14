<template>
  <div class="container-fluid">
    <div class="row my-5 justify-content-around">
      <div class="col-lg-5">
        <nuxt-link to="/pengunjung/tambah">
          <div class="card bg-pengunjung rounded-5">
            <div class="card-body">
            <h2 style="font-family: ;">pengunjung</h2>
            </div>
          </div>
        </nuxt-link>
  </div>

  <div class="col-lg-5">
    <nuxt-link to="/buku">
      <div class="card bg-buku rounded-5">
        <div class="card-body">
          <img src="~/assets/img/pencarian.png" alt="logo">
          <h2 style="font-family: ;">cari bg-buku</h2>
        </div>
      </div>
    </nuxt-link>
  </div>
  </div>
  </div>
</template>

<style scoped>
.card {
  height: 250px;
  box-shadow: 1px 1px 1px #424242;
}
.card.bg-pengunjung {
  background-image: url('../assets/img/bg-home-kunjungan.jpeg');
  background-repeat: no-repeat;
  background-position:center center;
  background-size: cover;
}
.card.bg-buku {
  background: url('../assets/img/bg-home-cari-buku7,jpeg') no-repeat center center;
  background-size: cover;
}
</style>