<template>
  <div class="container w-full">
    <Header />
    <Faq />
    <ColorSquare />
    <MintWrapper />
  </div>
</template>

<script>
import MintWrapper from '../components/MintWrapper.vue';

export default {
  name: 'VaraColors'
}
</script>

<style>
body {
  background-color: black;
  min-width: 100vw;
}

.container {
  align-items: center;
  max-width: 100vw;
}
</style>