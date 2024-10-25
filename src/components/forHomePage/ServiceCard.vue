<template>
  <li class="services__card">
    <div class="services__wrapper-img">
      <img :src="src" class="services__img">
    </div>
    <p class="services__desk">{{ text }}</p>
  </li>
</template>

<script>
export default {
  name: 'ServiceCard',
  data() {
    return {
      id: this.infoAboutCard['id'],
      src: require(`@/assets/img/forCardsOnHomePage/${this.infoAboutCard['src']}`),
      // src: `src/assets/img/forCardsOnHomePage/${this.infoAboutCard['src']}`,
      text: this.infoAboutCard['text']
    };
  },
  methods: {
    // Ваши методы здесь
  },
  components: {
  },
  props:['infoAboutCard']
};
</script>

<style scoped>
.services__card {
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #fff;
  padding: 15px;
}
.services__wrapper-img {
  max-width: 350px;
  max-height: 350px;
  overflow: hidden;
}
.services__wrapper-img:hover .services__img {
  transform: scale(1.1);
}
.services__img {
  transition: .5s;
}
.services__desk {
  margin-top: 16px;
  font-size: 24px;
  color: #3c3c3c;
  font-weight: 300;
  text-align: center;
}
</style>