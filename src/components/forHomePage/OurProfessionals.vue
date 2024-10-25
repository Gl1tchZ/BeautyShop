<template>
  <div class="professionals">
    <div class="professionals-wrapper">
      <p class="professionals__title">Our Professionals</p>
      <ul class="professionals__list">
        <CardProfessionals v-for="(professional, index) in professionals" :key="professional.id" :infoAboutCard="professionals[index]"/>
      </ul>
    </div>
  </div>
</template>

<script>
import CardProfessionals from './CardProfessionals.vue';

export default {
  name: 'OurProfessionals',
  data() {
    return {
      professionals: [
        {id: 1, src: '1.jpg', name: 'Sophia Anderson', position: 'Manager'},
        {id: 2, src: '2.jpg', name: 'Sophia Gill', position: 'Pedicure Expert'},
        {id: 3, src: '3.jpg', name: 'Anna Smith', position: 'Manicure Expert'},
        {id: 4, src: '4.jpg', name: 'Keth Jenner', position: 'Nail Artist'},
        {id: 5, src: '5.jpg', name: 'Anna Will', position: 'Senior Stylist'},
        {id: 6, src: '6.jpg', name: 'Jenny Tom', position: 'Nail Specialistis'}
      ]
    };
  },
  methods: {
    // Ваши методы здесь
  },
  components: {
    CardProfessionals
  }
};
</script>

<style scoped>
.professionals {
  padding: 80px 60px;
}
.professionals-wrapper {
}
.professionals__title {
  font-size: 56px;
  color: #3c3c3c;
  text-align: center;
  font-weight: 200;
  margin-bottom: 50px;
}
.professionals__list {
  display: flex;
  justify-content: space-between;
}
.professionals__item:first-child {
  display: block;
  padding-left: 0;
}
.professionals__item:last-child {
  padding-right: 0;
}
</style>