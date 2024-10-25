<template>
  <form class="form-section__wrapper">
    <p class="form-section__title">Make An Appointment</p>
    <p class="form-section__subtitle">Call: 666 333 9999 or Fill in the form below</p>
    <ul class="form-section__list">
      <li class="form-section__item"><input type="text" class="form-section__inp form-child" placeholder="Write Your Name Here" name="name"></li>
      <li class="form-section__item"><input type="email" class="form-section__inp form-child" placeholder="Write Your Email Here" name="email"></li>
      <li class="form-section__item"><input type="number" class="form-section__inp form-child" placeholder="Contact Number" name="number"></li>
      <li class="form-section__item"><input type="number" class="form-section__inp form-child" placeholder="No of people" name="noofpeople"></li>
      <li class="form-section__item"><input type="date" class="form-section__inp form-child" name="date"></li>
      <li class="form-section__item"><input type="time" class="form-section__inp form-child" name="time"></li>
      <li class="form-section__item form-section__item--textarea"><textarea class="form-child" placeholder="Your message" name="message"></textarea></li>
    </ul>
    <button type="submit" class="form-section__btn" @click="checkForm">BOOK NOW</button>
  </form>
</template>

<script>


// $.fn.checkForm = function() {
// let obj = new Object
// $(this).find('input').each((ind, i)=>{
// if (!obj.hasOwnProperty($(i).attr('data-type'))) {
// obj[$(i).attr('data-type')] = new Array
// }
// if ($(i).val() == '') {
// obj[$(i).attr('data-type')].push(null)
// } else if ($(i).attr('type') == 'file') {
// obj[$(i).attr('data-type')].push($(i)[0].files[0])
// } else {
// obj[$(i).attr('data-type')].push($(i).val())
// }
// })
// return obj
// }

export default {
  name: 'FormSection',
  data() {
    return {
      dataForm: []
    };
  },
  methods: {
    checkForm (e){
      e.preventDefault()
      document.querySelectorAll('.form-child').forEach((item) => {
        console.log(item);
        
      });
    }
  },
  components: {
  }
};
</script>

<style>
.form-section__wrapper {
  flex-direction: column;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 100px 60px;
  background-image: url("../../assets/img/forCardsOnHomePage/background.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.form-section__title {
  text-align: center;
  font-size: 56px;
  color: #3c3c3c;
  text-align: center;
  font-weight: 200;
  margin-bottom: 15px;
}
.form-section__subtitle {
  color: #797876;
  font-size: 18px;
  font-weight: 300;
  margin-bottom: 45px;
}
.form-section__list {
  width: 60%;
  display: grid;
  justify-items: center;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: repeat(3, 70px) 150px;
  grid-gap: 24px;
}
.form-section__item {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
}
.form-section__inp {
  font-size: 18px;
  font-weight: 300;
  color: #797876;
  width: 100%;
  border: none;
  padding: 20px 20px 20px 24px;
  outline: none;
}
.form-section__item--textarea {
  grid-column: 1/3;
}
.form-section__item--textarea textarea {
  width: 100%;
  height: 100%;
  resize: none;
  font-size: 18px;
  font-weight: 300;
  color: #797876;
  width: 100%;
  border: none;
  padding: 20px 20px 20px 24px;
  outline: none;
}
.form-section__btn {
  background-color: #df97a2;
  border: none;
  padding: 15px 35px;
  text-transform: uppercase;
  color: #fff;
  font-size: 18px;
  letter-spacing: 0.1rem;
  cursor: pointer;
  transition: .3s;
  margin-top: 50px;
}
.form-section__btn:hover {
  background-color: #df808f;
}
</style>