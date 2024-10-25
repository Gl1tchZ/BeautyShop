<template>
  <li class="commtents__item">
    <img :src="src" class="comments__img">
    <div class="commnets__text-block">
      <p class="comments__desk">{{ text }}</p>
      <p class="comments__title">{{ name }}</p>
      <p class="comments__desk">{{ desk }}</p>
    </div>
  </li>
</template>

<script>
export default {
  name: 'CommentUser',
  data() {
    return {
      id: this.infoAboutComment['id'],
      name: this.infoAboutComment['name'],
      text: this.infoAboutComment['text'],
      desk: this.infoAboutComment['desk'],
      src: require(`@/assets/img/gallaryComments/${this.infoAboutComment['src']}`)
    };
  },
  methods: {
  },
  components: {
  },
  props: ['infoAboutComment']
};
</script>

<style>
.commtents__item {
  min-width: 100%;
  padding: 0 50px;
  display: flex;
  align-items: center;
}
.comments__img {
  border-radius: 50%;
}
.commnets__text-block {
  margin-left: 24px;
}
.comments__desk {
  color: #797876;
  font: 18px;
}
.comments__title {
  color: #3c3c3c;
  margin: 16px 0;
  font-size: 32px;
}
</style>