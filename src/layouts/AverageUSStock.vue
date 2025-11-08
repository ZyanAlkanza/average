<template>
    <div class="row" style="overflow: hidden;">
      <div class="q-px-md col-12">
        <div class="col-2" style="height: 100%; border-radius: 16px;">
          <div class="content row justify-between">
            <div class="transaction col-md-4 col-xs-12 q-py-md q-px-sm">
              <div class="card-1 q-pa-md bg-grey-2" style="border-radius: 4px;">
                Transaction 1
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="lembar1" label="Total Shares" class="col-6"  mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled v-model="harga1" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
                </div>
              </div>

              <div class="card-2 q-pa-md q-mt-md bg-grey-2" style="border-radius: 4px;">
                Transaction 2
                <div class="row q-col-gutter-x-sm q-mt-md">
                  <q-input dense square filled v-model="lembar2" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled v-model="harga2" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi3 == false" v-model="lembar3" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi3 == false" v-model="harga3" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi4 == false" v-model="lembar4" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi4 == false" v-model="harga4" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi5 == false" v-model="lembar5" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi5 == false" v-model="harga5" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi6 == false" v-model="lembar6" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi6 == false" v-model="harga6" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi7 == false" v-model="lembar7" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi7 == false" v-model="harga7" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi8 == false" v-model="lembar8" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi8 == false" v-model="harga8" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi9 == false" v-model="lembar9" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi9 == false" v-model="harga9" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
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
                  <q-input dense square filled :disable="transaksi10 == false" v-model="lembar10" label="Total Shares" class="col-6" mask="#.##########"/>
                  <q-input dense square input-class="text-right" filled :disable="transaksi10 == false" v-model="harga10" label="Buy Price" class="col-6" prefix="$" mask="#.###.##" reverse-fill-mask/>
                </div>
              </div>
            </div>

            <div class="result col-md-4 col-xs-12 q-px-sm q-pt-md">
              <div class="bg-grey-2" style="border-radius: 8px;">
                <div class="title q-py-md flex justify-center items-end">
                  Your Average Stock Price :
                </div>
                <div class="title flex justify-center q-pt-sm text-primary" style="font-size: 32px; font-weight: bold;">
                  $ {{ average  }}
                </div>
                <div class="title q-py-md flex justify-center items-end">
                  Total Shares : {{ totalShares }}
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
      lembar1:'',
      lembar2:'',
      lembar3:'',
      lembar4:'',
      lembar5:'',
      lembar6:'',
      lembar7:'',
      lembar8:'',
      lembar9:'',
      lembar10:'',
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
      totallembar: 0,
      totalShares: 0
    }
  },
  methods: {
    hitung() {
      const harga1 = this.harga1
      const harga2 = this.harga2
      const harga3 = this.harga3
      const harga4 = this.harga4
      const harga5 = this.harga5
      const harga6 = this.harga6
      const harga7 = this.harga7
      const harga8 = this.harga8
      const harga9 = this.harga9
      const harga10 = this.harga10

      const transaksi1 = (parseFloat(this.lembar1) || 0) * (parseFloat(harga1) || 0);
      const transaksi2 = (parseFloat(this.lembar2) || 0) * (parseFloat(harga2) || 0);
      const transaksi3 = (this.lembar3 && this.harga3) ? (parseFloat(this.lembar3) || 0) * (parseFloat(harga3) || 0) : 0;
      const transaksi4 = (this.lembar4 && this.harga4) ? (parseFloat(this.lembar4) || 0) * (parseFloat(harga4) || 0) : 0;
      const transaksi5 = (this.lembar5 && this.harga5) ? (parseFloat(this.lembar5) || 0) * (parseFloat(harga5) || 0) : 0;
      const transaksi6 = (this.lembar6 && this.harga6) ? (parseFloat(this.lembar6) || 0) * (parseFloat(harga6) || 0) : 0;
      const transaksi7 = (this.lembar7 && this.harga7) ? (parseFloat(this.lembar7) || 0) * (parseFloat(harga7) || 0) : 0;
      const transaksi8 = (this.lembar8 && this.harga8) ? (parseFloat(this.lembar8) || 0) * (parseFloat(harga8) || 0) : 0;
      const transaksi9 = (this.lembar9 && this.harga9) ? (parseFloat(this.lembar9) || 0) * (parseFloat(harga9) || 0) : 0;
      const transaksi10 = (this.lembar10 && this.harga10) ? (parseFloat(this.lembar10) || 0) * (parseFloat(harga10) || 0) : 0;

      const totallembar = 
      (parseFloat(this.lembar1) || 0) + 
      (parseFloat(this.lembar2) || 0) +
      (parseFloat(this.lembar3) || 0) + 
      (parseFloat(this.lembar4) || 0) + 
      (parseFloat(this.lembar5) || 0) +
      (parseFloat(this.lembar6) || 0) +
      (parseFloat(this.lembar7) || 0) +
      (parseFloat(this.lembar8) || 0) +
      (parseFloat(this.lembar9) || 0) +
      (parseFloat(this.lembar10) || 0);
      const total = (transaksi1 + transaksi2 + transaksi3 + transaksi4 + transaksi5 + transaksi6 + transaksi7 + transaksi8 + transaksi9 + transaksi10) / (totallembar || 1);

      this.average = total.toFixed(2);
      this.totalShares = totallembar;
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
        this.lembar1='',
        this.lembar2='',
        this.lembar3='',
        this.lembar4='',
        this.lembar5='',
        this.lembar6='',
        this.lembar7='',
        this.lembar8='',
        this.lembar9='',
        this.lembar10='',
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
        this.totalShares= 0
      });
    }
  },
}
</script>
