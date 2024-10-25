<template>
  <div class="price-wrapper">
    <p class="price-wrapper__title">Price Packages</p>
    <ul class="price-wrapper__list">
      <li class="price-wrapper__item">
        <ul class="price__list">
          <CardPricePackage v-for="(card, index) in cards.slice(0, Math.ceil(cards.length / 2))" :key="card.id" :infoAboutCard="cards[index]"/>
        </ul>
      </li>
      <li class="price-wrapper__item">
        <ul class="price__list">
          <CardPricePackage v-for="(card, index) in cards.slice(Math.floor(cards.length / 2))" :key="card.id" :infoAboutCard="cards[index]"/>
        </ul>
      </li>
    </ul>
  </div>
</template>

<script>
import CardPricePackage from './CardPricePackage.vue';


export default {
  name: 'PricePackages',
  data() {
    return {
      cards: [
        {id: 1, title: 'Gel Nail Extensions', price: '130.00', src: '1.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'},
        {id: 2, title: 'Manicure', price: '100.00', src: '2.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'},
        {id: 3, title: 'Eyelashes Extensions', price: '120.00', src: '3.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'},
        {id: 4, title: 'Pedicure', price: '180.00', src: '4.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'},
        {id: 5, title: 'Facial Treatment', price: '120.00', src: '5.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'},
        {id: 6, title: 'Paraffin For Nail Hands', price: '130.00', src: '6.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'},
        {id: 7, title: 'Nail Art', price: '100.00', src: '7.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'},
        {id: 8, title: 'Nail Polishing', price: '180.00', src: '8.jpg', desk: 'Fugit eligendi non consectetur maxime accusantium possimus. Quia eos minusquo sed totam similique quas. Dolorum, nihil.'}
      ]
    };
  },
  methods: {
  },
  components: {
    CardPricePackage
  }
};
</script>

<style>
.price-wrapper {
  padding: 150px 60px;
  background-image: url("../../assets/img/back.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.price-wrapper__title {
  text-align: center;
  font-size: 56px;
  color: #3c3c3c;
  font-weight: 200;
  margin-bottom: 90px;
}
.price-wrapper__list {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-gap: 50px;
}
.price-wrapper__item {
}
.price__list {
}
</style>