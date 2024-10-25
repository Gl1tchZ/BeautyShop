<template>
  <PromoBlock/>
  <AdvantagesSection/>
  <ServicesBlock/>
  <AdSection/>
  <OurProfessionals/>
  <!-- <PopularProducts/> -->
  <PricePackages/>
  <ViewGallery/>
  <CommentsUser/>
  <FormSection/>
</template>

<script>
import PromoBlock from './forHomePage/PromoBlock.vue';
import AdvantagesSection from './forHomePage/AdvantagesSection.vue';
import ServicesBlock from './forHomePage/ServicesBlock.vue';
import AdSection from './forHomePage/AdSection.vue';
import OurProfessionals from './forHomePage/OurProfessionals.vue';
import PricePackages from './forHomePage/PricePackages.vue';
import ViewGallery from './forHomePage/ViewGallery.vue';
import CommentsUser from './forHomePage/CommentsUser.vue';
import FormSection from './forHomePage/FormSection.vue';
// // import PopularProducts from './forHomePage/PopularProducts.vue';

export default {
  name: 'HomePage',
  data() {
    return {
      // Ваши данные здесь
    };
  },
  methods: {
    // Ваши методы здесь
  },
  components: {
    PromoBlock,
    AdvantagesSection,
    ServicesBlock,
    AdSection,
    OurProfessionals,
    // PopularProducts,
    PricePackages,
    ViewGallery,
    CommentsUser,
    FormSection
  }
};
</script>

<style>
  
</style>