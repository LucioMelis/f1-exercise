<template>
  <div>
    <img :src="imgUrl(pilotiF1[0].numeroPilota)" alt="pilota" />
    <div>{{ pilotiF1 }}</div>
    <p>Ciao</p>
    <!-- <img :src="require(pilotiF1[0].numeroPilota2)" alt="pilota" /> -->
  </div>
</template>

<script>
import pilotiF1 from "@/assets/data/drivers.json";
export default {
  name: "MainComponents",
  data() {
    return {
      pilotiF1,
    };
  },
  methods: {
    imgUrl(img) {
      console.log(img);
      return require(`@/assets/${img}`);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
</style>
