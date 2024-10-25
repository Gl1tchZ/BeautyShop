<template>
  <div class="gallery-wrapper">
    <p class="gallery-wrapper__title">View Gallery</p>
    <ul class="gallery-wrapper__list">
      <li 
        class="gallery-wrapper__item" 
        v-for="(img, index) in imgs" 
        :key="img.id" 
        :style="{
          backgroundImage: 'url(' + require(`@/assets/img/viewGallary/${img.src}`) + ')',
          gridArea: classes[index]
        }"
        :id="img.id"
        @click="showPictures">
      </li>
    </ul>
    <div class="gallery-wrapper__big-img hide" @click="hidePictures">
      <div class="gallery-wrapper__btn gallery-wrapper__btn--prev">
        <svg class="gallery-wrapper__svg gallery-wrapper__svg--prev" @click="slidePictures">
          <use href="../../assets/sprite.svg#arrow"></use>
        </svg>
      </div>
      <div class="gallery-wrapper__img-wrapper">
        <img :src="checkedImg" class="gallery-wrapper__img">
      </div>
      <div class="gallery-wrapper__btn gallery-wrapper__btn--next">
        <svg class="gallery-wrapper__svg gallery-wrapper__svg--next" @click="slidePictures">
          <use href="../../assets/sprite.svg#arrow"></use>
        </svg>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ViewGallery',
  data() {
    return {
      checkedImg: '',
      checkedImgId: 0,
      imgs: [
        {id: 1, src: '1.jpg'},
        {id: 2, src: '2.jpg'},
        {id: 3, src: '3.jpg'},
        {id: 4, src: '4.jpg'},
        {id: 5, src: '5.jpg'},
        {id: 6, src: '4.jpg'},
      ],
      classes: ['small-one', 'big', 'small-two', 'medium-one', 'medium-two', 'small-three']
    };
  },
  methods: {
    showPictures (e){
      this.checkedImg = require(`@/assets/img/viewGallary/${this.imgs[e.target.id - 1].src}`)
      this.checkedImgId = e.target.id - 1
      let wrapperBigImg = document.querySelector('.gallery-wrapper__big-img')
      wrapperBigImg.classList.toggle('hide')
      setTimeout(() => {
        wrapperBigImg.style.opacity = 1;
        document.querySelector('body').style.overflowY = 'hidden'
      }, 100);
    },
    hidePictures (e){
      if (e.target.classList.contains('gallery-wrapper__big-img')) {
        document.querySelector('body').style.overflowY = 'scroll'
        e.target.style.opacity = 0;
        setTimeout(() => {
          e.target.classList.toggle('hide')
        }, 100);
      }
    },
    slidePictures(e) {
      if (e.target.classList.contains('gallery-wrapper__svg--next')) {
        if (this.checkedImgId+1 < this.imgs.length) {
          this.checkedImgId++
          this.checkedImg = require(`@/assets/img/viewGallary/${this.imgs[this.checkedImgId].src}`)
        } else {
          this.checkedImgId = 0
          this.checkedImg = require(`@/assets/img/viewGallary/${this.imgs[this.checkedImgId].src}`)
        }
      } else {
        if (this.checkedImgId == 0) {
          this.checkedImgId = this.imgs.length
          this.checkedImgId--
          this.checkedImg = require(`@/assets/img/viewGallary/${this.imgs[this.checkedImgId].src}`)
        } else {
          this.checkedImgId--
          this.checkedImg = require(`@/assets/img/viewGallary/${this.imgs[this.checkedImgId].src}`)
        }
      }
    }
  }
};
</script>

<style>
.gallery-wrapper {
  padding: 100px 60px;
}
.gallery-wrapper__title {
  text-align: center;
  font-size: 56px;
  color: #3c3c3c;
  text-align: center;
  font-weight: 200;
  margin-bottom: 50px;
}
.gallery-wrapper__list {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: 300px 300px 300px;
  grid-template-areas: 'small-one big small-two'
  'medium-one big medium-two'
  'medium-one small-three medium-two';
  grid-gap: 25px;
}
.gallery-wrapper__item {
  cursor: pointer;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}


.gallery-wrapper__big-img {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  padding: 0 25px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: rgba(0, 0, 0, 0.8);
  opacity: 0;
  transition: .3s;
  pointer-events: all;
}
.gallery-wrapper__btn {
  color: #fff;
}
.gallery-wrapper__svg {
  width: 50px;
  height: 50px;
  padding: 10px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  fill: #fff;
  background-color: rgba(0, 0, 0, .4);
  cursor: pointer;
}
.gallery-wrapper__svg--next {
  transform: rotate(180deg);
}
.gallery-wrapper__svg--prev {
}
.gallery-wrapper__btn--prev {
}
.gallery-wrapper__img-wrapper {
}
.gallery-wrapper__img {
  max-width: 80%;
  max-height: 90vh;
  width: auto;
  height: auto;
}
.gallery-wrapper__btn--next {
}


.hide {
  display: none;
}
</style>