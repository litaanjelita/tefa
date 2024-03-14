<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-lg-12">
        <h2 class="text-center-my-4">isi buku kunjungan</h2>
        <form>
          <div class="mb-3">
            <input type="text" class="form-control-lg form-select rounded-5" placeholder="NAMA...">
          </div>
          <div class="mb-3">
            <select class="form-control form-control form-select rounded-5">
              <option value="">KATEGORI</option>
              <option value="siswa">siswa</option>
              <option value="guru">guru</option>
              <option value="staff">staff</option>
              <option value="umum">umum</option>
            </select>
          </div>
          <div class="mb-3">
            <select class="form-control form-control form-select rounded-5">
              <option value="">KELAS</option>
              <option value="1">X</option>
              <option value="2">XI</option>
              <option value="3">XII</option>
            </select>
          </div>
          <div class="mb-3">
            <select class="form-control form-control form-select rounded-5">
              <option value="">KEPERLUAN</option>
              <option value="baca">baca</option>
              <option value="pinjam">pinjam</option>
              <option value="kembalikan">kembalikan buku</option>
            </select>
          </div>
          <nuxt-link to="../pengunjung"><button type="submit" class="btn btn-primary btn-lg rounded-5 px-5">KIRIM</button></nuxt-link>
          <nuxt-link to="../"><button type="submit" class="btn btn-secondary btn-lg rounded-5 px-5" style="margin-left: 82.5%;">KEMBALI</button></nuxt-link>
        </form>
      </div>
    </div>
  </div>
</template>