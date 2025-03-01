<template>
    <div class="row" style="height: 100dvh; overflow: hidden;">
      <div class="col-2 q-pa-md" v-show="menu">
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
      <div class="q-pa-md" :class="menu ? 'col-10' : 'col-12'">
        <div class="col-2 q-py-sm" style="height: 100%; border-radius: 16px;">
          <div class="content-title row justify-between" style="font-size: 20px;">
            <div>
              Hitung Harga Beli Rata-Rata
            </div>
            <div>
              <q-btn outline icon="menu" text-color="primary" @click="menu = !menu"/>
            </div>
          </div>
          <div class="content row justify-between">
            <div class="transaction col-6 q-py-md">
              <div class="card-1 q-pa-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 1
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="koin1" label="Jumlah Koin" class="col-6"  mask="#.########"/>
                  <q-input dense square filled v-model="harga1" label="Harga Per 1 Koin" class="col-6" prefix="Rp." mask="# ### ### ###"/>
                </div>
              </div>

              <div class="card-2 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaksi 2
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="koin2" label="Jumlah Koin" class="col-6" mask="#.########"/>
                  <q-input dense square filled v-model="harga2" label="Harga Per 1 Koin" class="col-6" prefix="Rp." mask="# ### ### ###"/>
                </div>
              </div>

              <div class="card-3 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaksi 3
                  </div>
                  <q-toggle
                    v-model="transaksi3"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi3 == false" v-model="koin3" label="Jumlah Koin" class="col-6" mask="#.########"/>
                  <q-input dense square filled :disable="transaksi3 == false" v-model="harga3" label="Harga Per 1 Koin" class="col-6" prefix="Rp." mask="# ### ### ###"/>
                </div>
              </div>

              <div class="card-4 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaksi 4
                  </div>
                  <q-toggle
                    v-model="transaksi4"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi4 == false" v-model="koin4" label="Jumlah Koin" class="col-6" mask="#.########"/>
                  <q-input dense square filled :disable="transaksi4 == false" v-model="harga4" label="Harga Per 1 Koin" class="col-6" prefix="Rp." mask="# ### ### ###"/>
                </div>
              </div>

              <div class="card-5 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaksi 5
                  </div>
                  <q-toggle
                    v-model="transaksi5"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi5 == false" v-model="koin5" label="Jumlah Koin" class="col-6" mask="#.########"/>
                  <q-input dense square filled :disable="transaksi5 == false" v-model="harga5" label="Harga Per 1 Koin" class="col-6" prefix="Rp." mask="# ### ### ###"/>
                </div>
              </div>

              <div class="row q-mt-sm q-gutter-sm">
                <q-btn outline disabled  color="primary" label="Tambah Transaksi" icon="add"/>
                <q-btn @click="hitung" class="col-grow" color="primary" label="Hitung Harga Rata-Rata" icon="calculate"/>
              </div>
            </div>
            <div class="result col-6 q-px-md q-pt-md">
              <div class="bg-grey-2" style="height: 30%; border-radius: 8px;">
                <div class="title flex justify-center items-end" style="height: 30%;">
                  Harga Rata-Rata Crypto-mu adalah:
                </div>
                <div class="title flex justify-center q-pt-lg text-primary" style="height: 70%; font-size: 32px; font-weight: bold;">
                  Rp. {{ average  }}
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      menu: false,
      koin1:'',
      koin2:'',
      koin3:'',
      koin4:'',
      koin5:'',
      harga1:'',
      harga2:'',
      harga3:'',
      harga4:'',
      harga5:'',
      transaksi3: false,
      transaksi4: false,
      transaksi5: false,
      average: 0
    }
  },
  methods: {
    hitung() {
      const harga1 = this.harga1.replace(/\s+/g,'');
      const harga2 = this.harga2.replace(/\s+/g,'');
      const harga3 = this.harga3.replace(/\s+/g,'');
      const harga4 = this.harga4.replace(/\s+/g,'');
      const harga5 = this.harga5.replace(/\s+/g,'');

      const transaksi1 = (parseFloat(this.koin1) || 0) * (parseFloat(harga1) || 0);
      const transaksi2 = (parseFloat(this.koin2) || 0) * (parseFloat(harga2) || 0);
      const transaksi3 = (this.koin3 && this.harga3) ? (parseFloat(this.koin3) || 0) * (parseFloat(harga3) || 0) : 0;
      const transaksi4 = (this.koin4 && this.harga4) ? (parseFloat(this.koin4) || 0) * (parseFloat(harga4) || 0) : 0;
      const transaksi5 = (this.koin5 && this.harga5) ? (parseFloat(this.koin5) || 0) * (parseFloat(harga5) || 0) : 0;

      const totalKoin = (parseFloat(this.koin1) || 0) + (parseFloat(this.koin2) || 0) + (parseFloat(this.koin3) || 0) + (parseFloat(this.koin4) || 0) + (parseFloat(this.koin5) || 0);
      const total = (transaksi1 + transaksi2 + transaksi3 + transaksi4 + transaksi5) / (totalKoin || 1);
      
      const konversiInteger = Math.floor(total);
      const konversiRupiah = konversiInteger.toLocaleString('id-ID');

      this.average = konversiRupiah;
    }
  },
}
</script>
