<template>
  <div class="w-tabs">
    <div>
      <v-tabs v-model="tab">
          <v-tab 
          v-for="item in tabs"
          :key="item.washComponent"
          >{{ item.title }}</v-tab>
      </v-tabs>
    </div>
    <div class="w-tabs-component">
      <v-tabs-items v-model="tab">
        <v-tab-item v-for="item in tabs" :key="item.washComponent">
          <component v-bind:is="item.washComponent" />
        </v-tab-item>
      </v-tabs-items>
    </div>
  </div>
</template>

<script>
import HistoryComponent from '../components/HistoryComponent.vue';
import PerfilComponent from '../components/PerfilComponent.vue';
import WalletComponent from '../components/WalletComponent.vue';


export default {
  name: 'HomeView',
  components: {
    HistoryComponent,
    PerfilComponent,
    WalletComponent
  },
  data() {
    return {
      tab: 'perfil',
      tabs: [
        { title: 'Inf. Pessoais', washComponent: 'PerfilComponent' },
        { title: 'Histórico', washComponent: 'HistoryComponent' },
        { title: 'Carteira', washComponent: 'WalletComponent' }
      ]
    }
  }
}
</script>

<style lang="scss">
.w-tabs {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  
  .w-tabs-component {
    width: 100%;
    height: 100%;
  }
}
</style>