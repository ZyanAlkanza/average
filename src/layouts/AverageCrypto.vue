<template>
    <div class="row" style="overflow: hidden;">
      <div class="q-px-md col-12">
        <div class="col-2" style="height: 100%; border-radius: 16px;">
          <div class="content row justify-between">
            <div class="transaction col-md-4 col-xs-12 q-py-md q-px-sm">
              <div class="card-1 q-pa-md bg-grey-2" style="border-radius: 4px;">
                Transaction 1
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="koin1" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled v-model="harga1" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>

              <div class="card-2 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaction 2
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="koin2" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled v-model="harga2" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>

              <div class="card-3 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 3
                  </div>
                  <q-toggle
                    v-model="transaksi3"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi3 == false" v-model="koin3" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi3 == false" v-model="harga3" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>

              <div class="card-4 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 4
                  </div>
                  <q-toggle
                    v-model="transaksi4"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi4 == false" v-model="koin4" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi4 == false" v-model="harga4" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>

              <div class="card-5 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 5
                  </div>
                  <q-toggle
                    v-model="transaksi5"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi5 == false" v-model="koin5" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi5 == false" v-model="harga5" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>
            </div>
            
            <div class="transaction col-md-4 col-xs-12 q-py-md q-px-sm">
              <div class="card-1 q-pa-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 6
                  </div>
                  <q-toggle
                    v-model="transaksi6"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi6 == false" v-model="koin6" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi6 == false" v-model="harga6" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>
              
              <div class="card-3 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 7
                  </div>
                  <q-toggle
                    v-model="transaksi7"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi7 == false" v-model="koin7" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi7 == false" v-model="harga7" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>

              <div class="card-3 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 8
                  </div>
                  <q-toggle
                    v-model="transaksi8"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi8 == false" v-model="koin8" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi8 == false" v-model="harga8" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>

              <div class="card-4 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 9
                  </div>
                  <q-toggle
                    v-model="transaksi9"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi9 == false" v-model="koin9" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi9 == false" v-model="harga9" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>

              <div class="card-5 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                <div class="flex justify-between">
                  <div class="flex justify-center items-center">
                    Transaction 10
                  </div>
                  <q-toggle
                    v-model="transaksi10"
                    color="primary"
                    dense
                  />
                </div>
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled :disable="transaksi10 == false" v-model="koin10" label="Total Coin" class="col-6"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi10 == false" v-model="harga10" label="Price Per Coin" class="col-6" prefix="Rp." mask="#.###.###.###" reverse-fill-mask maxlength="13"/>
                </div>
              </div>
            </div>

            <div class="result col-md-4 col-xs-12 q-px-sm q-pt-md">
              <div class="bg-grey-2" style="border-radius: 8px;">
                <div class="title q-py-md flex justify-center items-end">
                  Your Average Coin Price :
                </div>
                <div class="title flex justify-center q-pt-sm text-primary" style="font-size: 32px; font-weight: bold;">
                  Rp. {{ average  }}
                </div>
                <div class="title q-py-md flex justify-center items-end">
                  Total Coin : {{ totalCoin }}
                </div>
              </div>
              <div class="row q-mt-sm q-gutter-sm">
                <q-btn outline @click="reset" class="col-grow"  color="primary" label="Reset" icon="restart_alt"/>
                <q-btn @click="hitung" class="col-grow" color="primary" label="Count The Average" icon="calculate"/>
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
      koin6:'',
      koin7:'',
      koin8:'',
      koin9:'',
      koin10:'',
      harga1:'',
      harga2:'',
      harga3:'',
      harga4:'',
      harga5:'',
      harga6:'',
      harga7:'',
      harga8:'',
      harga9:'',
      harga10:'',
      transaksi3: false,
      transaksi4: false,
      transaksi5: false,
      transaksi6: false,
      transaksi7: false,
      transaksi8: false,
      transaksi9: false,
      transaksi10: false,
      average: 0,
      totalCoin: 0
    }
  },
  methods: {
    hitung() {
      const harga1 = this.harga1.replace(/\./g,'');
      const harga2 = this.harga2.replace(/\./g,'');
      const harga3 = this.harga3.replace(/\./g,'');
      const harga4 = this.harga4.replace(/\./g,'');
      const harga5 = this.harga5.replace(/\./g,'');
      const harga6 = this.harga6.replace(/\./g,'');
      const harga7 = this.harga7.replace(/\./g,'');
      const harga8 = this.harga8.replace(/\./g,'');
      const harga9 = this.harga9.replace(/\./g,'');
      const harga10 = this.harga10.replace(/\./g,'');

      const transaksi1 = (parseFloat(this.koin1) || 0) * (parseFloat(harga1) || 0);
      const transaksi2 = (parseFloat(this.koin2) || 0) * (parseFloat(harga2) || 0);
      const transaksi3 = (this.koin3 && this.harga3) ? (parseFloat(this.koin3) || 0) * (parseFloat(harga3) || 0) : 0;
      const transaksi4 = (this.koin4 && this.harga4) ? (parseFloat(this.koin4) || 0) * (parseFloat(harga4) || 0) : 0;
      const transaksi5 = (this.koin5 && this.harga5) ? (parseFloat(this.koin5) || 0) * (parseFloat(harga5) || 0) : 0;
      const transaksi6 = (this.koin6 && this.harga6) ? (parseFloat(this.koin6) || 0) * (parseFloat(harga6) || 0) : 0;
      const transaksi7 = (this.koin7 && this.harga7) ? (parseFloat(this.koin7) || 0) * (parseFloat(harga7) || 0) : 0;
      const transaksi8 = (this.koin8 && this.harga8) ? (parseFloat(this.koin8) || 0) * (parseFloat(harga8) || 0) : 0;
      const transaksi9 = (this.koin9 && this.harga9) ? (parseFloat(this.koin9) || 0) * (parseFloat(harga9) || 0) : 0;
      const transaksi10 = (this.koin10 && this.harga10) ? (parseFloat(this.koin10) || 0) * (parseFloat(harga10) || 0) : 0;

      const totalKoin = 
      (parseFloat(this.koin1) || 0) + 
      (parseFloat(this.koin2) || 0) + 
      (parseFloat(this.koin3) || 0) + 
      (parseFloat(this.koin4) || 0) + 
      (parseFloat(this.koin5) || 0) +
      (parseFloat(this.koin6) || 0) +
      (parseFloat(this.koin7) || 0) +
      (parseFloat(this.koin8) || 0) +
      (parseFloat(this.koin9) || 0) +
      (parseFloat(this.koin10) || 0);
      const total = (transaksi1 + transaksi2 + transaksi3 + transaksi4 + transaksi5 + transaksi6 + transaksi7 + transaksi8 + transaksi9 + transaksi10) / (totalKoin || 1);
      
      const konversiInteger = Math.floor(total);
      const konversiRupiah = konversiInteger.toLocaleString('id-ID');

      this.average = konversiRupiah;
      this.totalCoin = totalKoin.toFixed(5);
    },
    reset() {
      this.$q.dialog({
        title: 'Reset Form',
        message: 'Are you sure want to reset this form?',
        ok: {
          flat: true,
          color: 'primary'
        },
        cancel: {
          flat: true,
          color: 'red'
        },
        persistent: true,
      }).onOk(() => {
        this.menu= false,
        this.koin1='',
        this.koin2='',
        this.koin3='',
        this.koin4='',
        this.koin5='',
        this.koin6='',
        this.koin7='',
        this.koin8='',
        this.koin9='',
        this.koin10='',
        this.harga1='',
        this.harga2='',
        this.harga3='',
        this.harga4='',
        this.harga5='',
        this.harga6='',
        this.harga7='',
        this.harga8='',
        this.harga9='',
        this.harga10='',
        this.transaksi3= false,
        this.transaksi4= false,
        this.transaksi5= false,
        this.transaksi6= false,
        this.transaksi7= false,
        this.transaksi8= false,
        this.transaksi9= false,
        this.transaksi10= false,
        this.average= 0,
        this.totalCoin= 0
      });
    }
  },
}
</script>
