<template>
  <div class="button-row">
    <button v-if="isConnected == false" class="connect-wallet-button" @click="connectWallet">Connect wallet</button>
    <button v-else class="connect-wallet-button">Mint Vara Color</button>
  </div>
</template>


<script>
//import { GearApi } from '@gear-js/api';

export default {
  data() {
    return {
      isConnected: false,
    };
  },
  methods: {
    connectWallet() {
      this.isConnected = true
    },
    async mintVaraColor() {
      // this function requires the library @gear-js/api which is not supported on deployment because of a webpack error
      const programAddress = "0xacf1987d2e17008191fa792e1b695d53170b6072d0418932ec12f090cd34892a"

      const tokenMetadata = {
        name: "VARA COLOR",
        description: "VARA Colors is a project made during Polkadot Prodigy hackaton. It's a collection of NFTs living on Vara testnet.",
        reference: "none",
        media: "none",
        word: document.getElementById('textInput').value,
        saturation: document.getElementById('saturationRange').value,
        light: document.getElementById('lightRange').value,
      }

      const payload = {
        Mint: {
          to: account?.decodedAddress,
          tokenMetadata,
        }
      };

      let extrinsic

      try {
        const message = {
          destination: programAddress,
          payload: payload,
          gasLimit: 10000000,
          value: 1000,
        };
        extrinsic = api.message.send(message, meta);
      } catch (error) {
        console.error(`${error.name}: ${error.message}`);
      }
      try {
        await extrinsic.signAndSend(keyring, (event) => {
          console.log(event.toHuman());
        });
      } catch (error) {
        console.error(`${error.name}: ${error.message}`);
      }
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
