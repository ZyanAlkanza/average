<template>
  <q-layout view="lHh Lpr lff" container style="height: 100dvh">
    <q-header class="bg-white">
      <q-toolbar class="justify-between">
        <span class="text-primary" style="font-size: 16px; font-weight: 500;">
          {{ activeMenu }}
          
          <q-btn
            class="text-grey-6"
            dense
            flat
            icon="error_outline"
            size="sm"
            @click="information"
          />
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
      <q-page v-show="activeMenu == 'Average Stock'">
        <AverageStock />
      </q-page>
      <q-page v-show="activeMenu == 'Average US Stock'">
        <AverageUSStock />
      </q-page>
    </q-page-container>

    <q-dialog v-model="averageCoinDialog">
      <q-card>
        <q-card-section>
          <div class="text-h6">Information</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          <q-img
            src="../assets/img/averageCoin.gif"
            style="width: 400px;"
            fit="fill"
          />
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
  </q-layout>
</template>

<script>
import AverageCrypto from './AverageCrypto.vue';
import AverageStock from './AverageStock.vue';
import AverageUSStock from './AverageUSStock.vue';

export default {
  components: {
    AverageCrypto,
    AverageStock,
    AverageUSStock
  },
  data() {
    return {
      averageStockDialog: false,
      averageUSStockDialog: false,
      averageCoinDialog: false,
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
    }
  },
  methods: {
    information() {
      if(this.activeMenu == 'Average Coin'){
        this.averageCoinDialog = true;
      }
    }
  },
}
</script>
