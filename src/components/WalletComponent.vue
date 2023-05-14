<template>
  <div class="w-wallet-container">
    <v-card class="w-wallet-card">
      <v-card-title class="w-wallet-title">
        <img src="../assets/card-credit.png" width="50" height="50"/>
        <h2 style="margin-left: 15px; color: #FFF">Carteira Virtual</h2>
      </v-card-title>
      <v-card-actions class="w-wallet-content" v-for="item in creditCards" :key="item.cardNumber" style="display: flex; flex-direction: column; justify-content: space-between; align-items: flex-start;">
        <div  class="w-credit-cards">
          <img src="../assets/single-card-credit.png" width="45" height="45"/>
          <div style="margin-left: 15px; text-align: left;">
            <p style="font-size: 11px;">Cartão Final: {{ item.cardNumber }}</p>
            <p style="font-size: 11px;">Nome Sobrenome: {{ item.name }}</p>
            <p style="font-size: 11px;">Vencimento: {{ item.invalidDate }}</p>
          </div>
        </div>
        <v-divider></v-divider>
      </v-card-actions>
    </v-card>
  </div>
</template>
  
<script>
  export default {
    name: 'WalletComponent',
    data() {
      return {
        creditCards: [
          { cardNumber: '**** 5560', name: 'John Doe', invalidDate: '12/2030' },
          { cardNumber: '**** 7340', name: 'John Doe', invalidDate: '02/2024' },
        ]
      }
    }
  }
</script>

<style lang="scss">
.w-wallet-container {
  display: flex;
  justify-content: center;
  margin-top: 50px;

  .w-wallet-card {
    width: 80%;
    .w-wallet-content {
      background-color: #E0F3F0;

      .w-credit-cards {
        display: flex;
        flex-direction: row;
        margin-top: 20px;
        margin-left: 20px;
      }
    }
    .w-wallet-title {
      background-color: #2FB9A0;
    }
  }
}
</style>