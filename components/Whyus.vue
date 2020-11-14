<template>
  <section class="why-us">
    <div class="container">
      <div class="why-title-wrapper row">
        <h1 class="why-title">Почему выбирают LikeIT school?</h1>
      </div>
      <swiper ref="mySwiper" class="why-slider-wrapper" :options="swiperOption">
        <swiper-slide class="why-inner">
          <div class="why-vs"><span> VS</span></div>

          <div class="why-inner-left">
            <h3 class="why-inner-left-top">Самостоятельно</h3>
            <h2 class="why-inner-left-title">с чего начать</h2>
            <p class="why-inner-left-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
          <div class="why-inner-right">
            <div class="why-inner-right-top">
              <img src="../assets/img/logo.svg" alt="" />
            </div>
            <h2 class="why-inner-right-title">проверенная программа</h2>
            <p class="why-inner-right-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
        </swiper-slide>
        <swiper-slide class="why-inner">
          <div class="why-vs"><span> VS</span></div>

          <div class="why-inner-left">
            <h3 class="why-inner-left-top">Самостоятельно</h3>
            <h2 class="why-inner-left-title">с чего начать</h2>
            <p class="why-inner-left-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
          <div class="why-inner-right">
            <div class="why-inner-right-top">
              <img src="../assets/img/logo.svg" alt="" />
            </div>
            <h2 class="why-inner-right-title">проверенная программа</h2>
            <p class="why-inner-right-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
        </swiper-slide>
        <swiper-slide class="why-inner">
          <div class="why-vs"><span> VS</span></div>

          <div class="why-inner-left">
            <h3 class="why-inner-left-top">Самостоятельно</h3>
            <h2 class="why-inner-left-title">с чего начать</h2>
            <p class="why-inner-left-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
          <div class="why-inner-right">
            <div class="why-inner-right-top">
              <img src="../assets/img/logo.svg" alt="" />
            </div>
            <h2 class="why-inner-right-title">проверенная программа</h2>
            <p class="why-inner-right-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
        </swiper-slide>
        <swiper-slide class="why-inner">
          <div class="why-vs"><span> VS</span></div>

          <div class="why-inner-left">
            <h3 class="why-inner-left-top">Самостоятельно</h3>
            <h2 class="why-inner-left-title">с чего начать</h2>
            <p class="why-inner-left-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
          <div class="why-inner-right">
            <div class="why-inner-right-top">
              <img src="../assets/img/logo.svg" alt="" />
            </div>
            <h2 class="why-inner-right-title">проверенная программа</h2>
            <p class="why-inner-right-text">
              Тут нужно что-нибудь классное написать побольше о том. что за
              ступени отбора такие.
            </p>
          </div>
        </swiper-slide>
       
      </swiper>
       <div class="why-slider-nav">
          <div class="why-pagination">
            <span></span>
          </div>
          <div class="why-arr why-arr__left" >
              <img src="../assets/img/arr-slider.svg" alt="">
          </div>
          <div class=" why-arr why-arr__right">
              <img src="../assets/img/arr-slider.svg" alt="">
          </div>
        </div>
        <div class="btn-wrapper">
          <button class="btn btn__header">Начать учиться</button>

        </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      swiperOption: {
        autoHeight: true,
        spaceBetween: 20,
        pagination: {
          el: ".why-pagination",
          clickable: true,
        },
        navigation: {
          nextEl: ".why-arr__right",
          prevEl: ".why-arr__left",
        },
      },
    };
  },
};
</script>
<style scoped>
</style>