<template>
  <li class="professionals__item">
    <div class="professionals__wrapper-img">
      <img :src="src" class="professionals__img">
      <div class="professionals__wrapper-svg">
        <svg class="professionals__svg" style="transition-delay: .2s;">
          <a href="#!">
            <use href="../../assets/sprite.svg#inst"></use>
          </a>
        </svg>
        <svg class="professionals__svg" style="transition-delay: .5s;">
          <a href="#!">
            <use href="../../assets/sprite.svg#twitter"></use>
          </a>
        </svg>
        <svg class="professionals__svg" style="transition-delay: .8s;">
          <a href="#!">
            <use href="../../assets/sprite.svg#facebook"></use>
          </a>
        </svg>
      </div>
    </div>
    <p class="professionals__title">{{ name }}</p>
    <p class="professionals__desk">{{ position }}</p>
  </li>
</template>

<script>

export default {
  name: 'CardProfessionals',
  data() {
    return {
      id: this.infoAboutCard['id'],
      src: require(`@/assets/img/forProfessionals/${this.infoAboutCard['src']}`),
      name: this.infoAboutCard['name'],
      position: this.infoAboutCard['position']
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
.professionals__item {
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 12px;
}
.professionals__wrapper-img {
  width: 250px;
  height: 280px;
  overflow: hidden;
  position: relative;
}
.professionals__wrapper-img:hover .professionals__img {
  transform: scale(1.1);
}
.professionals__wrapper-img:hover .professionals__svg {
  transform: rotateY(0);
}
.professionals__img {
  cursor: pointer;
  transition: .5s;
}
.professionals__wrapper-svg {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 10;
  display: flex;
  flex-direction: column;
}
.professionals__svg {
  background-color: #e09aa5;
  width: 30px;
  height: 30px;
  transform-origin: left;
  transform: rotateY(90deg);
  padding: 10px;
  box-sizing: content-box;
  transition: .3s;
}
.professionals__svg use {
  fill: #fff;
}
.professionals__title {
  margin: 16px;
  font-size: 24px;
  font-weight: 300;
  color: #3c3c3c;
  text-align: center;
  transition: .3s;
  cursor: pointer;
}
.professionals__title:hover {
  color: #e09aa5;
}
.professionals__desk {
  text-align: center;
  color: #787672;
  font-weight: 300;
}
</style>