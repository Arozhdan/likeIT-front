<template>
  <div>
    <header class="thanks-header">
      <Nav />
      <div class="thanks-header-inner">
        <img src="../assets/img/doggy.png" alt="" />
      </div>
    </header>
    <section class="thanks">
      <div class="container">
        <h1 class="thanks-title">Благодарим за Покупку!</h1>
        <h2 class="thanks-suptitle"> <img src="../assets/img/check.svg" alt=""> Оплата прошла успешно.</h2>
        <p class="thanks-text">
          Мы выслали Вам подтверждение об оплате на электронную почту. В
          ближайшее время наши специалисты свяжутся с вами. <br><br> Если у вас возникнут
          какие-либо вопросы, вы всегда можете написать или позвонить нам!
          Пожалуйста, обратите внимание, что рабочее время нашей школы с пн-пт с
          9:00 до 20:00 по московскому времени.
        </p>
        <div class="btn-wrapper">
          <button class="btn btn__thanks">Написать нам</button>
        </div>
      </div>
    </section>
    <Footer />
  </div>
</template>
<script>
import Nav from "../components/Nav";
import Footer from "../components/Footer";
export default {
  components: {
    Nav,
    Footer,
  },
};
</script>