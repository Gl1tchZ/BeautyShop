<template>
  <div class="services">
    <div class="content-wrapper">
      <p class="services__title">Services We Offer</p>
      <ul class="services__list">
        <ServiceCard v-for="(card, index) in cards" :key="card.id" :infoAboutCard="cards[index]"/>
      </ul>
      <button class="services__btn">See All Services</button>
    </div>
  </div>
</template>

<script>
import ServiceCard from './ServiceCard.vue';

export default {
  name: 'ServicesBlock',
  data() {
    return {
      cards: [
        {id: 1, src: '1.jpg', text: 'Hydra Facial'},
        {id: 2, src: '2.jpg', text: 'Art Nail & Effects'},
        {id: 3, src: '3.jpg', text: 'Paraffin For Nail Hands'},
        {id: 4, src: '4.jpg', text: 'Glitter For Nail Art'},
        {id: 5, src: '5.jpg', text: 'Classic Nail Manicure'},
        {id: 6, src: '6.jpg', text: 'Eyelashes Extensions'},
        {id: 7, src: '7.jpg', text: 'Pedicure'},
        {id: 8, src: '8.jpg', text: 'Deep Paraffin Waxing'},
      ]
    };
  },
  methods: {
  },
  components: {
    ServiceCard
  }
};
</script>

<style scoped>
.services {
  background-image: url("../../assets/img/forCardsOnHomePage/background.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed
}
.content-wrapper {
  padding: 180px 60px;
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
}
.services__title {
  font-size: 56px;
  font-weight: 200;
  text-align: center;
}
.services__list {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  width: 100%;
  grid-gap: 50px;
  margin: 80px 0;
}
.services__btn {
  background-color: #df97a2;
  padding: 18px 35px;
  text-transform: uppercase;
  color: #fff;
  font-size: 17px;
  font-weight: 600;
  border: none;
  cursor: pointer;
  transition: .3s;
}
.services__btn:hover {
  background-color: #df808f;
}
</style>