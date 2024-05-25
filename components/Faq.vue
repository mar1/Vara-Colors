<template>
  <div class="faq">
    <ul>
      <li v-for="(faq, index) in faqs" :key="index" @click="toggleFaq(index)">
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
        { question: "What is VARA Colors?", answer: "Vue.js is a progressive JavaScript framework for building user interfaces.", open: false },
        { question: "How do I mint VARA Colors?", answer: "You can install Vue.js via CDN, npm, or by downloading the library.", open: false },
        { question: "What tech VARA Colors is using?", answer: "A component in Vue.js is a reusable instance with a name.", open: false },
        { question: "What's the roadmap for VARA Colors?", answer: "A component in Vue.js is a reusable instance with a name.", open: false },
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
