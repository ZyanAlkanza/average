<template>
  <q-layout view="lHh Lpr lff" container style="height: 100dvh">
    <q-header class="bg-white">
      <q-toolbar class="justify-between">
        <span class="text-primary" style="font-size: 16px; font-weight: 500;">
          {{ activeMenu }}
        </span>
        <q-btn 
          icon="widgets" 
          class="text-primary"
          @click="menu = !menu" 
          flat 
          round 
          dense 
        >
          <q-tooltip
            transition-show="scale"
            transition-hide="scale"  
          >
            Sidemenu
          </q-tooltip>
        </q-btn>
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="menu"
      show-if-above
      :width="250"
      :breakpoint="500"
      class="q-pa-sm"
    >
      <q-scroll-area class="fit bg-primary rounded-borders q-pa-sm">
        <q-list class="q-py-sm q-mb-lg">
          <q-img
            src="../assets/logo.png"
            fit="contain"
            :ratio="16/9"
            height="5dvh"
          />
        </q-list>
        <q-list>
          <template v-for="(menuItem, index) in menuList" :key="index">
            <q-item 
              clickable 
              :active="menuItem.label === activeMenu" 
              :class="menuItem.label === activeMenu ? 'text-black bg-white rounded-borders' : 'text-white rounded-borders'"
              @click="activeMenu = menuItem.label"
              >
              <q-item-section avatar>
                <q-icon :name="menuItem.icon"/>
              </q-item-section>
              <q-item-section>
                {{ menuItem.label }}
              </q-item-section>
            </q-item>
          </template>

        </q-list>
      </q-scroll-area>
    </q-drawer>

    <q-page-container>
      <q-page v-show="activeMenu == 'Average Coin'">
        <AverageCrypto />
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script>
import AverageCrypto from './AverageCrypto.vue';

export default {
  components: {
    AverageCrypto
  },
  data() {
    return {
      menu: false,
      activeMenu:'Average Coin',
      menuList: [
        {
          'label': 'Average Stock',
          'icon': 'trending_up'
        },
        {
          'label': 'Average US Stock',
          'icon': 'trending_up'
        },
        {
          'label': 'Average Coin',
          'icon': 'paid'
        },
      ],
      // koin1:'',
      // koin2:'',
      // koin3:'',
      // koin4:'',
      // koin5:'',
      // harga1:'',
      // harga2:'',
      // harga3:'',
      // harga4:'',
      // harga5:'',
      // transaksi3: false,
      // transaksi4: false,
      // transaksi5: false,
      // average: 0
    }
  },
  methods: {
    // hitung() {
    //   const harga1 = this.harga1.replace(/\s+/g,'');
    //   const harga2 = this.harga2.replace(/\s+/g,'');
    //   const harga3 = this.harga3.replace(/\s+/g,'');
    //   const harga4 = this.harga4.replace(/\s+/g,'');
    //   const harga5 = this.harga5.replace(/\s+/g,'');

    //   const transaksi1 = (parseFloat(this.koin1) || 0) * (parseFloat(harga1) || 0);
    //   const transaksi2 = (parseFloat(this.koin2) || 0) * (parseFloat(harga2) || 0);
    //   const transaksi3 = (this.koin3 && this.harga3) ? (parseFloat(this.koin3) || 0) * (parseFloat(harga3) || 0) : 0;
    //   const transaksi4 = (this.koin4 && this.harga4) ? (parseFloat(this.koin4) || 0) * (parseFloat(harga4) || 0) : 0;
    //   const transaksi5 = (this.koin5 && this.harga5) ? (parseFloat(this.koin5) || 0) * (parseFloat(harga5) || 0) : 0;

    //   const totalKoin = (parseFloat(this.koin1) || 0) + (parseFloat(this.koin2) || 0) + (parseFloat(this.koin3) || 0) + (parseFloat(this.koin4) || 0) + (parseFloat(this.koin5) || 0);
    //   const total = (transaksi1 + transaksi2 + transaksi3 + transaksi4 + transaksi5) / (totalKoin || 1);
      
    //   const konversiInteger = Math.floor(total);
    //   const konversiRupiah = konversiInteger.toLocaleString('id-ID');

    //   this.average = konversiRupiah;
    // }
  },
}
</script>
