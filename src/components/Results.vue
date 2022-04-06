<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  }, //when this mounts to the DOM it will check the ranks
  mounted() {
    if (this.score < 200) {
      this.rank = "Ninja Fingers";
    } else if (this.score < 400) {
      this.rank = "Rocket Reflexes";
    } else {
      this.rank = "Snail pace..";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4rem;
  color: #0faf87;
  font-weight: bold;
}
</style>