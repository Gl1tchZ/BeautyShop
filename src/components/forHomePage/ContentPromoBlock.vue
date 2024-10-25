<template>
  <div class="content-wrapper">
    <svg class="main-block__svg main-block__svg--left" @click="swapPictures">
      <use href="../../assets/sprite.svg#arrow"></use>
    </svg>
    <div class="main-block__text-block">
      <p class="text-block__title">Embark on a journey of self-care and elegance</p>
      <button class="text-block__btn">Get an Appointment</button>
    </div>
    <svg class="main-block__svg main-block__svg--right" @click="swapPictures">
      <use href="../../assets/sprite.svg#arrow"></use>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'ContentPromoBlock',
  data() {
    return {
    };

  },
  methods: {
    sendData(data) {
      this.$emit('updatePositionBackground', data);
    },
    swapPictures(e) {
      let background = this.positionBackground
      if (e.target.classList.contains('main-block__svg--left')) {
        if (background == 1) {
          this.sendData(3)
        } else {
          background--
          this.sendData(background)
        } 
      } else {
        if (background == 3) {
          this.sendData(1)
        } else {
          background++
          this.sendData(background)
        } 
      }
    }
  },
  components: {

  },
  props: ['positionBackground']
};
</script>

<style scoped>
.content-wrapper {
  width: 100vw;
  padding: 0 60px;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.main-block__text-block {
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
}
.text-block__title {
  max-width: 900px;
  text-align: center;
  text-transform: capitalize;
  font-size: 72px;
  color: #fff;
  font-weight: 300;
}
.text-block__btn {
  margin-top: 25px;
  padding: 25px 35px;
  background-color: #df97a2;
  border: none;
  text-transform: uppercase;
  font-weight: 600;
  letter-spacing: 0.2rem;
  color: #fff;
  font-size: 18px;
  cursor: pointer;
  transition: .3s;
}
.text-block__btn:hover {
  background-color: #df808f;
}
.main-block__svg {
  width: 50px;
  fill: #fff;
  opacity: .3;
  transition: .3s;
  cursor: pointer;
}
.main-block__svg:hover {
  opacity: 1;
}
.main-block__svg--left {
}
.main-block__svg--right {
  transform: rotate(180deg);
}
</style>
