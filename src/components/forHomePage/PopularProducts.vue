<template>
  <div class="popular-products">
    <div class="popular-products-wrapper">
      <div class="popular-products__header-products">
        <p class="header-products__title">Popular Products</p>
        <button class="header-products__btn">VIEW ALL</button>
      </div>
      <div class="popular-products__wrapper-list">
        <ul class="popular-products__list">
          <CardPopularProducts v-for="(product, index) in products" :key="product.id" :infoAboutCard="products[index]" :infoAboutFrame="infoWidthFrame"/>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import CardPopularProducts from './CardPopularProducts.vue';

export default {
  name: 'PopularProducts',
  data() {
    return {
      products: [
        {id: 1, name:'Gel Nail Polish', src: '1.jpg', price: '95.00'},
        {id: 2, name:'Gel Nail Polish', src: '2.jpg', price: '95.00'},
        {id: 3, name:'Gel Nail Polish', src: '3.jpg', price: '95.00'},
        {id: 4, name:'Gel Nail Polish', src: '4.jpg', price: '95.00'},
        {id: 5, name:'Gel Nail Polish', src: '5.jpg', price: '95.00'},
        {id: 6, name:'Gel Nail Polish', src: '6.jpg', price: '95.00'},
        {id: 7, name:'Gel Nail Polish', src: '7.jpg', price: '95.00'},
      ],
      infoWidthFrame: 500
    };
  },
  methods: {
    frameWidth(){
      let wrapper = document.querySelector('.popular-products__list')
      this.infoWidthFrame = wrapper.offsetWidth / 5;
      console.log(this.infoWidthFrame);
    }
  },
  components: {
    CardPopularProducts
  }
};
</script>

<style scoped>
.popular-products {

}
.popular-products-wrapper {
  padding: 100px 60px;
}
.popular-products__header-products {
  display: flex;
  justify-content: space-between;
  margin-bottom: 50px;
}
.header-products__title {
  font-size: 56px;
  color: #3c3c3c;
  text-align: center;
  font-weight: 200;
}
.header-products__btn {
  background-color: #df97a2;
  border: none;
  padding: 15px 35px;
  text-transform: uppercase;
  color: #fff;
  font-size: 18px;
  letter-spacing: 0.1rem;
  cursor: pointer;
}
.header-products__btn:hover {
  background-color: #df808f;
}
.popular-products__wrapper-list {
  overflow: visible;
}
.popular-products__list {
  /* max-width: 100%; */
  overflow: visible;
  display: flex;
  grid-gap: 30px;
  /* justify-content: space-between; */
}
</style>