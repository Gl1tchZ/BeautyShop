<template>
  <header class="header">
    <section class="header__contact-block">
      <div class="header-wrapper">
        <div class="contact-block__list">
          <li class="contact-block__item">
            <svg class="contact-block__svg">
              <use href="../assets/sprite.svg#location"></use>
            </svg>
            <p class="contact-block__desk">State Road 54 Trinity, Florida</p>
          </li>
          <li class="contact-block__item">
            <svg class="contact-block__svg">
              <use href="../assets/sprite.svg#call"></use>
            </svg>
            <p class="contact-block__desk">call: 666 333 9999</p>
          </li>
        </div>
        <ul class="contact-block__list">
          <p class="contact-block__desk">Follow us:</p>
          <li class="contact-block__item">
            <a href="#!" class="contact-block__link">
              <svg class="contact-block__svg">
                <use href="../assets/sprite.svg#facebook"></use>
              </svg>
            </a>
          </li>
          <li class="contact-block__item">
            <a href="#!" class="contact-block__link">
              <svg class="contact-block__svg">
                <use href="../assets/sprite.svg#inst"></use>
              </svg>
            </a>
          </li>
          <li class="contact-block__item">
            <a href="#!" class="contact-block__link">
              <svg class="contact-block__svg">
                <use href="../assets/sprite.svg#twitter"></use>
              </svg>
            </a>
          </li>
        </ul>
      </div>
    </section>
    <section class="header__main-block">
      <div class="header-wrapper">
        <div class="main-block__wrapper-logo">
          <img src="../assets/img/logo.png" class="logo">
        </div>
        <nav class="main-block-nav">
          <ul class="main-block-nav__list">  
            <li class="main-block-nav__item">
              <a href="#!" class="main-block-nav__link">Home</a>
            </li>
            <li class="main-block-nav__item">
              <a href="#!" class="main-block-nav__link">Shop</a>
            </li>
            <li class="main-block-nav__item">
              <a href="#!" class="main-block-nav__link">Services</a>
            </li>
            <li class="main-block-nav__item">
              <a href="#!" class="main-block-nav__link">Blog</a>
            </li>
            <li class="main-block-nav__item">
              <a href="#!" class="main-block-nav__link">Contact</a>
            </li>
            <li class="main-block-nav__item">
              <svg class="main-block-nav__svg">
                <use href="../assets/sprite.svg#search"></use>
              </svg>
            </li>
          </ul>
        </nav>
      </div>
    </section>
  </header>
</template>

<script>
export default {
  name: 'HeaderPage',
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
.header {
  height: 120px;
}
.header-wrapper {
  padding: 0 60px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.header__contact-block {
  padding: 5px 0;
  background-color: #f9e4e3;
}
.contact-block__list {
  display: flex;
  list-style: none;
}
.contact-block__item {
  margin-right: 0.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
}
.contact-block__desk {
  margin-right: 16px;
  font-weight: 300;
}
.contact-block__svg {
  width: 18px;
  height: 18px;
  fill: #575757;
  margin-right: 8px;
  transition: .2s;
}
.contact-block__svg:hover {
  fill: #df97a2;
}
.contact-block__link {
}
.header__main-block {
  padding: 16px 0;
}
.main-block-nav__list {
  display: flex;
}
.main-block-nav__item {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 16px;
}
.main-block-nav__link {
  font-size: 16px;
  font-weight: 300;
  text-transform: uppercase;
  transition: .3s;
  border-bottom: 1px solid #fff;
  box-sizing: border-box;
}
.main-block-nav__link:hover {
  color: #df97a2;
  border-bottom: 1px solid #df97a2;
}
.main-block-nav__svg {
  margin-left: 16px;
  width: 24px;
  height: 24px;
  transform: rotate(-90deg);
  fill: #df97a2;
  cursor: pointer;
}
</style>