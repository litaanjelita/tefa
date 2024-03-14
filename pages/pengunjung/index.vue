<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <h2 class="text-center my-4">RIWAYAT KUNJUNGAN</h2>
        <div class="my-3">
          <input type="search" class="form-control form-control-lg rounded-5" placeholder="FILTER...">
        </div>
        <div class="my-3 text-muted">menampilkan 1 dari 1</div>
        <table class="table">
          <thead>
            <tr>
              <td>#</td>
              <td>NAMA</td>
              <td>KEANGGOTAAN</td>
              <td>WAKTU</td>
              <td>KEPERLUAN</td>
            </tr>
          </thead>
          <tr>
            <td>1</td>
            <td>LITA ANJELITA</td>
            <td>SISWA</td>
            <td>26 FEBRUARI 2024, 12.00</td>
            <td>MEMBACA</td>
          </tr>
        </table>
        <nuxt-link to="../pengunjung/tambah">
          <button type="submit" class="btn btn-secondary btn-lg rounded-5 px-5" style="margin-left: 90.5%;">KEMBALI</button>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>