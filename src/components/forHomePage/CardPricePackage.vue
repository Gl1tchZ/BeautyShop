<template>
  <li class="price__item">
    <img :src="src" class="price__img">
    <div class="price__info-block">
      <div class="price__title-block">
        <p class="price__title">{{ title }}</p>
        <p class="price__subtitle">${{ price }}</p>
      </div>
      <p class="price__desk">{{ desk }}</p>
    </div>
  </li>
</template>

<script>
export default {
  name: 'CardPricePackage',
  data() {
    return {
      id: this.infoAboutCard['id'],
      src: require(`@/assets/img/forPrice/${this.infoAboutCard['src']}`),
      title: this.infoAboutCard['title'],
      price: this.infoAboutCard['price'],
      desk: this.infoAboutCard['desk'],
    };
  },
  methods: {

  },
  components: {

  },
  props: ['infoAboutCard']
};
</script>

<style>
.price__item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: .3s;
  cursor: pointer;
  background-color: #fff;
  padding: 50px;
}
.price__item:hover {
  background-color: #f8f9fa;
}
.price__img {
  min-width: 100px;
  max-width: 100px;
  min-height: 100px;
  max-height: 100px;
  border-radius: 50%;
  margin-right: 10px;
}
.price__info-block {
  width: 80%;
}
.price__title-block {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 0 10px 0;
}
.price__title {
  color: #3c3c3c;
  font-size: 24px;
}
.price__subtitle {
  color: #3c3c3c;
  font-weight: 400;
}
.price__desk {
  color: #797876;
}
</style>