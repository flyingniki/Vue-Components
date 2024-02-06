<script>
import BasketSelect from "./BasketSelect.vue";
import BasketFavorite from "./BasketFavorite.vue";
import BasketRemove from "./BasketRemove.vue";
import Counter from "../../ui/Counter.vue";

export default {
  components: {
    BasketSelect,
    BasketFavorite,
    BasketRemove,
    Counter,
  },
};
</script>

<template>
  <div class="basket-item">
    <BasketSelect />
    <div class="basket-item__detail"></div>
    <Counter />
    <div class="basket-item__price"></div>
    <BasketFavorite />
    <BasketRemove />
  </div>
</template>

<style lang="sass">
.basket-item
    width: 1015px
</style>
