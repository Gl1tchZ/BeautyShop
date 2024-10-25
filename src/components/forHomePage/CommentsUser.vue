<template>
  <div class="wrapper">
    <div class="comments-wrapper">
      <ul class="commtents__list">
        <CommentUser v-for="(comment, index) in comments" :key="comment.id" :infoAboutComment="comments[index]"/>
      </ul>
      <ul class="commnets__btn-list" @click="switchImage">
        <li class="comments__btn-item" :class="{ 'comments__btn-item--active': index === 0 }" v-for="(comment, index) in comments" :key="comment.id"></li>
      </ul>
    </div>
  </div>
</template>

<script>
import CommentUser from './CommentUser.vue';

export default {
  name: 'CommentsUser',
  data() {
    return {
      comments: [
        {id: 1, text: '“Pretium turpis faucibus adipiscing duis. Id quis tristique mi vitae nec. In et in praesentpellentesque. Porta sit porta ridiculus faucibus. Curabitur lacus pretium pellentesque interdumurna blandit.”', name: 'Jenny Will', desk:'Hanay mom', src: '1.jpg'},
        {id: 2, text: '“Pretium turpis faucibus adipiscing duis. Id quis tristique mi vitae nec. In et in praesentpellentesque. Porta sit porta ridiculus faucibus. Curabitur lacus pretium pellentesque interdumurna blandit.”', name: 'Emily Smith', desk:'Serene mom', src: '2.jpg'},
        {id: 2, text: '“Pretium turpis faucibus adipiscing duis. Id quis tristique mi vitae nec. In et in praesentpellentesque. Porta sit porta ridiculus faucibus. Curabitur lacus pretium pellentesque interdumurna blandit.”', name: 'Emily Smith', desk:'Serene mom', src: '2.jpg'},
        {id: 3, text: '“Pretium turpis faucibus adipiscing duis. Id quis tristique mi vitae nec. In et in praesentpellentesque. Porta sit porta ridiculus faucibus. Curabitur lacus pretium pellentesque interdumurna blandit.”', name: 'Noran Shara', desk:'Sam mom', src: '3.jpg'}
      ]
    };
  },
  methods: {
    switchImage (e){
      let activeBtn = e.target
      let slide = document.querySelector('.commtents__item')
      let slideWrapper = document.querySelector('.commtents__list')
      document.querySelectorAll('.comments__btn-item').forEach((item, ind) => {
        item.classList.remove('comments__btn-item--active')
        if (activeBtn == item) {
          item.classList.add('comments__btn-item--active')
          slideWrapper.style.transform = `translate(-${slide.offsetWidth*ind}px)`
        }
      });
    }
  },
  components: {
    CommentUser
  }
};
</script>

<style>
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  /* margin: 20px 0; */
  padding: 100px 60px;
  background-image: url("../../assets/img/backgroundForPromo/1.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.comments-wrapper {
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #fff;
  width: 80%;
  padding: 50px 0;
  box-sizing: content-box;
  overflow: hidden;
}
.commtents__list {
  display: flex;
  transition: .5s;
  /* margin: 50px 100px; */
}
.commnets__btn-list {
  display: flex;
  justify-content: space-between;
  margin-top: 50px;
}
.comments__btn-item {
  cursor: pointer;
  width: 20px;
  height: 20px;
  background-color: #f9e4e3;
  border-radius: 50%;
  transition: .3s;
  margin: 0 10px;
}
.comments__btn-item:hover {
  background-color: #df97a2;
}
.comments__btn-item:first-child {
  margin-left: 0;
}
.comments__btn-item:last-child {
  margin-right: 0;
}
.comments__btn-item--active {
  background-color: #df97a2;
}
</style>