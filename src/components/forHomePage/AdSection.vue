<template>
  <div class="adSection">
    <div class="adSection-wrapper">
      <div class="adSection__text-block">
        <p class="adSection__title">Most Popular, Clean, And Recommended Nail Salon</p>
        <p class="adSection__desk">Pretium turpis faucibus adipiscing duis. Id quis tristique mi vitae nec. In et in praesent pellentesque. Porta sit porta ridiculus faucibus. Curabitur lacus pretium pellentesque interdum urna blandit.</p>
        <ul class="adSection__list">
          <li class="adSection__item">Lorem ipsum dolor, sit amet consectetur adipisicing elit.</li>
          <li class="adSection__item">Fugiat aliquid qui quia provident unde cumque excepturi enim.</li>
          <li class="adSection__item">Saepe ipsum quam sed corporis aut voluptate quaerat quo quisquam.</li>
        </ul>
        <button class="adSection__btn">About Us</button>
      </div>
      <div class="adSection__img-block">
        <img src="../../assets/img/about.jpg" class="adSection__img">
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'AdSection',
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
.adSection {
  padding: 180px 60px;
}
.adSection-wrapper {
  display: grid;
  grid-template-columns: 900px 1fr;
}
.adSection__text-block {
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: flex-start;
}
.adSection__title {
  font-size: 56px;
  font-weight: 200;
  color: #3c3c3c;
}
.adSection__desk {
  margin: 16px 0;
  line-height: 30px;
  color: #797876;
  font-weight: 300;
}
.adSection__list {
  margin-bottom: 16px;
}
.adSection__item {
  line-height: 25px;
  font-size: 18px;
  font-weight: 300;
  padding-left: 32px;
  position: relative;
}
.adSection__item::after {
  content: '';
  width: 5px;
  height: 5px;
  background-color: #797876;
  position: absolute;
  top: 50%;
  left: 15px;
  border-radius: 50%;
  transform: translateY(-50%);
}
.adSection__btn {
  background-color: #df97a2;
  border: none;
  padding: 15px 35px;
  text-transform: uppercase;
  color: #fff;
  font-size: 18px;
  letter-spacing: 0.1rem;
  cursor: pointer;
}
.adSection__img-block {
}
.adSection__img {
}
</style>