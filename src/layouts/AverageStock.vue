<template>
    <div class="row" style="overflow: hidden;">
      <div class="q-px-md col-12">
        <div class="col-2" style="height: 100%; border-radius: 16px;">
          <div class="content row justify-between">
            <div class="transaction col-md-4 col-xs-12 q-py-md q-px-sm">
              <div class="card-1 q-pa-md bg-grey-2" style="border-radius: 4px;">
                Transaction 1
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="lot1" label="Total Lot" class="col-6"  mask="#####"/>
                  <q-input dense square input-class="text-right" filled v-model="harga1" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
                </div>
              </div>

              <div class="card-2 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaction 2
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="lot2" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled v-model="harga2" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi3 == false" v-model="lot3" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi3 == false" v-model="harga3" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi4 == false" v-model="lot4" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi4 == false" v-model="harga4" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi5 == false" v-model="lot5" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi5 == false" v-model="harga5" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi6 == false" v-model="lot6" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi6 == false" v-model="harga6" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi7 == false" v-model="lot7" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi7 == false" v-model="harga7" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi8 == false" v-model="lot8" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi8 == false" v-model="harga8" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi9 == false" v-model="lot9" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi9 == false" v-model="harga9" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi10 == false" v-model="lot10" label="Total Lot" class="col-6" mask="#####"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi10 == false" v-model="harga10" label="Buy Price" class="col-6" prefix="Rp." mask="#.###.###" reverse-fill-mask/>
                </div>
              </div>
            </div>

            <div class="result col-md-4 col-xs-12 q-px-sm q-pt-md">
              <div class="bg-grey-2" style="border-radius: 8px;">
                <div class="title q-py-md flex justify-center items-end">
                  Your Average Stock Price :
                </div>
                <div class="title flex justify-center q-pt-sm text-primary" style="font-size: 32px; font-weight: bold;">
                  Rp. {{ average  }}
                </div>
                <div class="title q-py-md flex justify-center items-end">
                  Total Shares : {{ totalShares }} / Total Lot: {{ totalLot }}
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
      lot1:'',
      lot2:'',
      lot3:'',
      lot4:'',
      lot5:'',
      lot6:'',
      lot7:'',
      lot8:'',
      lot9:'',
      lot10:'',
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
      totalLot: 0,
      totalShares: 0
    }
  },
  methods: {
    hitung() {
      const harga1 = this.harga1.replace('.','');
      const harga2 = this.harga2.replace('.','');
      const harga3 = this.harga3.replace('.','');
      const harga4 = this.harga4.replace('.','');
      const harga5 = this.harga5.replace('.','');
      const harga6 = this.harga6.replace('.','');
      const harga7 = this.harga7.replace('.','');
      const harga8 = this.harga8.replace('.','');
      const harga9 = this.harga9.replace('.','');
      const harga10 = this.harga10.replace('.','');

      const transaksi1 = (parseInt(this.lot1) || 0) * (parseInt(harga1) || 0);
      const transaksi2 = (parseInt(this.lot2) || 0) * (parseInt(harga2) || 0);
      const transaksi3 = (this.lot3 && this.harga3) ? (parseInt(this.lot3) || 0) * (parseInt(harga3) || 0) : 0;
      const transaksi4 = (this.lot4 && this.harga4) ? (parseInt(this.lot4) || 0) * (parseInt(harga4) || 0) : 0;
      const transaksi5 = (this.lot5 && this.harga5) ? (parseInt(this.lot5) || 0) * (parseInt(harga5) || 0) : 0;
      const transaksi6 = (this.lot6 && this.harga6) ? (parseInt(this.lot6) || 0) * (parseInt(harga6) || 0) : 0;
      const transaksi7 = (this.lot7 && this.harga7) ? (parseInt(this.lot7) || 0) * (parseInt(harga7) || 0) : 0;
      const transaksi8 = (this.lot8 && this.harga8) ? (parseInt(this.lot8) || 0) * (parseInt(harga8) || 0) : 0;
      const transaksi9 = (this.lot9 && this.harga9) ? (parseInt(this.lot9) || 0) * (parseInt(harga9) || 0) : 0;
      const transaksi10 = (this.lot10 && this.harga10) ? (parseInt(this.lot10) || 0) * (parseInt(harga10) || 0) : 0;

      const totalLot = 
      (parseInt(this.lot1) || 0) + 
      (parseInt(this.lot2) || 0) +
      (parseInt(this.lot3) || 0) + 
      (parseInt(this.lot4) || 0) + 
      (parseInt(this.lot5) || 0) +
      (parseInt(this.lot6) || 0) +
      (parseInt(this.lot7) || 0) +
      (parseInt(this.lot8) || 0) +
      (parseInt(this.lot9) || 0) +
      (parseInt(this.lot10) || 0);
      const total = (transaksi1 + transaksi2 + transaksi3 + transaksi4 + transaksi5 + transaksi6 + transaksi7 + transaksi8 + transaksi9 + transaksi10) / (totalLot || 1);
      
      const konversiInteger = Math.floor(total);
      const konversiRupiah = konversiInteger.toLocaleString('id-ID');

      this.average = konversiRupiah;
      this.totalLot = totalLot;
      this.totalShares = totalLot * 100;
    },
    reset() {
      this.$q.dialog({
        title: 'Reset Form',
        message: 'Are you sure ?',
        cancel: true,
        persistent: true,
      }).onOk(() => {
        this.lot1='',
        this.lot2='',
        this.lot3='',
        this.lot4='',
        this.lot5='',
        this.lot6='',
        this.lot7='',
        this.lot8='',
        this.lot9='',
        this.lot10='',
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
        this.totalLot= 0,
        this.totalShares= 0
      });
    }
  },
}
</script>
