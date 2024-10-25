<template>
  <div class="main-block" :style="{ backgroundImage: 'url(' + imageSrc + ')' }">
    <div class="main-block-wrapper">
      <ContentPromoBlock :positionBackground="backgroundImage" @updatePositionBackground="updateBackground"/>
    </div>
  </div>
</template>

<script>
import ContentPromoBlock from './ContentPromoBlock.vue';

export default {
  name: 'PromoBlock',
  data() {
    return {
      backgroundImage: 1,
      imageSrc: require(`@/assets/img/backgroundForPromo/1.png`)
    };
  },
  methods: {
    updateBackground(newBackground) {
      this.backgroundImage = newBackground
      this.imageSrc = require(`@/assets/img/backgroundForPromo/${newBackground}.png`)
    }
  },
  components: {
    ContentPromoBlock
  }
};
</script>

<style scoped>
.main-block {
  display: flex;
  justify-content: center;
  align-items: center;
  height: calc(100vh - 120px);
  background-image: url('../../assets/img/backgroundForPromo/1.png');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  transition: .3s;
  background-attachment: fixed;
}
.main-block-wrapper {
}
</style>