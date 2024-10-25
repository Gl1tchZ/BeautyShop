<template>
  <div class="content-wrapper">
    <ul class="advantages__list">
      <li class="advantages__item">
        <svg class="advantages__svg">
          <use href="../../assets/sprite.svg#medal"></use>
        </svg>
        <p class="advantages__title">10+ Years Of Experience</p>
        <p class="advantages__subtitle">Lorem ipsum dolor sit amet, consectetur adipi elit. Lorem ipsum dolor sit.</p>
      </li>
      <li class="advantages__item">
        <svg class="advantages__svg">
          <use href="../../assets/sprite.svg#plant"></use>
        </svg>
        <p class="advantages__title">100% Natural Products</p>
        <p class="advantages__subtitle">Lorem ipsum dolor sit amet, consectetur adipi elit. Lorem ipsum dolor sit.</p>
      </li>
      <li class="advantages__item">
        <svg class="advantages__svg">
          <use href="../../assets/sprite.svg#like"></use>
        </svg>
        <p class="advantages__title">10+ Years Of Experience</p>
        <p class="advantages__subtitle">Lorem ipsum dolor sit amet, consectetur adipi elit. Lorem ipsum dolor sit.</p>
      </li>
      <li class="advantages__item">
        <svg class="advantages__svg">
          <use href="../../assets/sprite.svg#people"></use>
        </svg>
        <p class="advantages__title">10+ Years Of Experience</p>
        <p class="advantages__subtitle">Lorem ipsum dolor sit amet, consectetur adipi elit. Lorem ipsum dolor sit.</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'AdvatagesSection',
  data() {
    return {
      // Ваши данные здесь
    };
  },
  methods: {
    // Ваши методы здесь
  },
  components: {
  }
};
</script>

<style scoped>
.content-wrapper {
  padding: 180px 60px;
}
.advantages__list {
  display: flex;
}
.advantages__item {
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
}
.advantages__svg {
  fill: #df97a2;
  width: 60px;
  height: 60px;
}
.advantages__title {
  color: #3c3c3c;
  font-size: 28px;
  text-align: center;
  font-weight: 300;
  margin: 25px 0;
}
.advantages__subtitle {
  font-weight: 300;
  color: #797876;
  font-size: 18px;
  text-align: center;
}
</style>