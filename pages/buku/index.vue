<template>
    <div class="container-fluid">
        <div class="row content">
            <div class="col-lg-12">
                <h2 class="text-center my-4" style="color: aliceblue;">RAK BUKU</h2>
                <div class="my-3 d-flex justify-content-center">
                    <input type="search" class="form-control rounded-5 cari" placeholder="SEARCH?..." style="background-color: #B0CFE5;">
                </div>
                <div class="my-3 text-muted"></div>
                <div class="row layer m-5 rounded-5">
                    <h1 class="text-center" style="color: aliceblue;">Koleksi Buku</h1>
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="../assets/img/cover1.jpg" class="cover" alt="cover 1" style="width: 100%;">
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="../assets/img/cover2.jpg" class="cover" alt="cover 2" style="width: 100%;">
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="../assets/img/cover3.jpeg" class="cover" alt="cover 3" style="width: 100%;">
                            </div>
                        </div>
                    </div>
                    <div class="col-lg-2">
                        <div class="card mb-3">
                            <div class="card-body">
                                <img src="../assets/img/cover4.jpg" class="cover" alt="cover 3" style="width: 100%;">
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style scoped>

.content {
    background-color: #658694;
}

.cari{
    width: 40rem;
}
/* .cover{
    height: 50%;
    width: 50%;
} */
.layer {
    background-color: #89B6D6;
}
</style>