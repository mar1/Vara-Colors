<template>
  <div class="button-row">
    <button v-if="isConnected == false" class="connect-wallet-button" @click="connectWallet">Connect wallet</button>
    <button v-else class="connect-wallet-button">Mint Vara Color</button>
  </div>
</template>


<script>

export default {
  data() {
    return {
      isConnected: false,
    };
  },
  methods: {
    connectWallet() {
      this.isConnected = true
    }

  },
};
</script>

<style scoped>
.button-row {
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  width: 100%;
}

.connect-wallet-button {
  padding: 10px 50px;
  font-size: 16px;
  cursor: pointer;
  color: white;
  border: 1px solid hsl(166, 100%, 50%);
  border-radius: 5%;
  font-family: 'Nocember';
}
</style>
