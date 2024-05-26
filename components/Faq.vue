<template>
  <div class="faq">
    <ul>
      <li class="mx-64 text-lg" v-for="(faq, index) in faqs" :key="index" @click="toggleFaq(index)">
        <span class="triangle" :class="{ open: faq.open }">></span>
        <span>{{ faq.question }}</span>
        <p v-if="faq.open">{{ faq.answer }}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      faqs: [
        { question: "What is VARA Colors?", answer: "VARA Colors is a project made during Polkadot Prodigy hackaton. It's a collection of NFTs living on Vara testnet. Every NFT has a color code made of a customizable saturation and light. You can choose for the text between white, black and vara color. Every attributes is fully stored on chain. Basically, there is no image, only blockchain attributes stored in the program's state.", open: false },
        { question: "What tech VARA Colors is using?", answer: "VARA Colors is using Rust for the smart-contract, Nuxt for the front-end and gear-api for the interaction with the chain.", open: false },
        { question: "What's the roadmap for VARA Colors?", answer: "The idea was to come first with a proof-of-concept for the hackaton. The NFTs are mintable. Second step would be to make the front-end better. Third step would be to put the NFTs on the main-net. Fourth step would be to use the VARA collected to stake and send the rewards to each owner proportionally to the number of NFTs holded.", open: false },
      ],
    };
  },
  methods: {
    toggleFaq(index) {
      this.faqs[index].open = !this.faqs[index].open;
    },
  },
};
</script>
