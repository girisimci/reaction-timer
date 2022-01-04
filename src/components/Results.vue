<template>
  <h2>Reaction Time - {{ score }} ms</h2>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Ninja gibisin";
    } else if (this.score < 400) {
      this.rank = "Tavşan reflexi...";
    } else {
      this.rank = "Kaplumbağa olmadığına emin misin?";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  color: green;
  font-weight: bold;
}
</style>
