<script>
export default {
  data() {
    return {};
  },
  methods: {
    btnClick() {
      console.log("click");
    },
  },
};
</script>

<template>
  <div class="card-description__button" v-on:click="btnClick">
    <img
      src="../../assets/img/inactive.png"
      alt=""
      class="card-description__button-img"
    />
  </div>
</template>

<style lang="sass" scoped>
.card-description__button {
  width: 44px;
  height: 44px;
  cursor: pointer;
}
</style>
