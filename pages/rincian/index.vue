<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <form>
                    <div class="col-md-8">
                        <div class="mb-3">
                            <input
                                type="text"
                                class="form-nama form-control form-control-lg rounded-5"
                                placeholder="NAMA"
                            />
                        </div>
                        <div class=" mb-3">
                            <select
                                V-model="keanggotaan"
                                    class="form-kategori form-control form-control-lg form-select rounded-5"
                                >
                                <option value="">KATEGORI</option>
                                <option>SISWA</option>
                                <option>GURU</option>
                                <option>Staf</option> 
                                <option>Umum</option>
                            </select>  
                        </div>
                        <div class="mb-3">
                            <select
                                class="form-keperluan form-control form-control-lg form-select rounded-5"
                                >
                                <option value="">KEPERLUAN</option>
                                <option value="baca">BACA BUKU</option>
                                <option value="pinjam">PINJAM BUKU</option>
                                <option value="kembalikan">KEMBALIKAN BUKU</option>
                                </select>
                        </div>
                    </div>
               </form>
            </div>
        </div>
    </div>
</template>