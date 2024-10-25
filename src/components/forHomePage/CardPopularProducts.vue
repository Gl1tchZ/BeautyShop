<template>
  <li class="popular-products__item" :style="{ width: widthBlock + 'px' }">
    <div class="popular-products__wrapper-img">
      <img :src="src" class="popular-products__img">
    </div>
    <div class="popular-products__wrapper-info">
      <a href="#!" class="popular-products__text popular-products__text--link">{{ name }}</a>
      <a href="#!" class="popular-products__text">{{ price }}</a>
    </div>
  </li>
</template>

<script>
export default {
  name: 'CardPopularProducts',
  data() {
    return {
      id: this.infoAboutCard['id'],
      name: this.infoAboutCard['name'],
      src: require(`@/assets/img/forPopularProducts/${this.infoAboutCard['src']}`),
      price: this.infoAboutCard['price'],
      widthBlock: this.infoAboutFrame
    };
  },
  methods: {
  },
  components: {
  },
  props: ['infoAboutCard', 'infoAboutFrame']
};
</script>

<style scoped>
.popular-products__item {
}
.popular-products__wrapper-img {
  /* width: 100%; */
  height: 350px;
  overflow: hidden;
}
.popular-products__img {
}
.popular-products__wrapper-info {
  display: flex;
  justify-content: space-between;
}
.popular-products__text {
}
.popular-products__text--link {
}
</style>