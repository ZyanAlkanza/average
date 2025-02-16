<template>
    <div class="row" style="height: 100vh; overflow: hidden;">
      <div class="col-2 q-pa-md">
        <div class="sidebar bg-primary" style="height: 100%; border-radius: 16px; padding: 32px 16px;">
          <div class="logo flex justify-center" style="width: 100%;">
            <img src="../assets/logo.png" alt="Average Logo" style="width: 70%;">
          </div>
          <div class="menu" style="margin-top: 56px;">
            <div class="bg-white q-pa-sm" style="border-radius: 8px;">
              <i class="ri-btc-line ri-lg"></i>
              Harga Rata-Rata
            </div>
          </div>
        </div>
      </div>
      <div class="col-10 q-pa-md">
        <div class="col-2 q-py-sm" style="height: 100%; border-radius: 16px;">
          <div class="content-title" style="font-size: 20px;">
            Hitung Harga Beli Rata-Rata
          </div>
          <div class="content row justify-between">
            <div class="transaction col-6 q-py-md">
              <div class="card-1 q-pa-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 1
                <div class="row q-col-gutter-x-sm q-mt-sm">
                  <q-input dense square filled v-model="text" label="Jumlah Koin" class="col-6" />
                  <q-input dense square filled v-model="text" label="Harga Per 1 Koin" class="col-6" />
                </div>
              </div>

              <div class="card-2 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 2
                <div class="row q-col-gutter-x-sm q-mt-sm">
                  <q-input dense square filled v-model="text" label="Jumlah Koin" class="col-6" />
                  <q-input dense square filled v-model="text" label="Harga Per 1 Koin" class="col-6" />
                </div>
              </div>

              <div class="card-3 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 3
                <div class="row q-col-gutter-x-sm q-mt-sm">
                  <q-input dense square filled v-model="text" label="Jumlah Koin" class="col-6" />
                  <q-input dense square filled v-model="text" label="Harga Per 1 Koin" class="col-6" />
                </div>
              </div>

              <div class="card-4 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 4
                <div class="row q-col-gutter-x-sm q-mt-sm">
                  <q-input dense square filled v-model="text" label="Jumlah Koin" class="col-6" />
                  <q-input dense square filled v-model="text" label="Harga Per 1 Koin" class="col-6" />
                </div>
              </div>

              <div class="card-5 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 5
                <div class="row q-col-gutter-x-sm q-mt-sm">
                  <q-input dense square filled v-model="text" label="Jumlah Koin" class="col-6" />
                  <q-input dense square filled v-model="text" label="Harga Per 1 Koin" class="col-6" />
                </div>
              </div>
              
              <!-- <div class="card-6 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 6
                <div class="row q-col-gutter-x-sm q-mt-sm">
                  <q-input dense square filled v-model="text" label="Jumlah Koin" class="col-6" />
                  <q-input dense square filled v-model="text" label="Harga Per 1 Koin" class="col-6" />
                </div>
              </div> -->

              <div class="row q-mt-sm q-gutter-sm">
                <div class="col-auto q-pa-sm" style="border-radius: 4px; background-color: #A1E3F9;">
                  <i class="ri-add-line ri-lg"></i>
                  Tambah Transaksi
                </div>

                <div class="col-grow bg-primary text-white text-center q-pa-sm" style="border-radius: 4px;">
                  <i class="ri-calculator-line ri-lg"></i>
                  Hitung Harga Rata-Rata
                </div>
              </div>
            </div>
            <div class="result col-6 q-px-md q-pt-md">
              <div class="bg-grey-2" style="height: 30%; border-radius: 8px;">
                <div class="title flex justify-center items-end" style="height: 30%;">
                  Harga Rata-Rata Crypto-mu adalah:
                </div>
                <div class="title flex justify-center q-pt-lg text-primary" style="height: 70%; font-size: 32px; font-weight: bold;">
                  Rp.1.000.000
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>

</script>
