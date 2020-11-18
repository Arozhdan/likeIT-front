<template>
  <section class="services">
    <div class="container">
      <h2 class="secondary-title">Программы и курсы LikeIT school</h2>
      <div class="row services-wrapper">
        <div class="services-item-persp">
          <div class="services-item services-item__1">
            <div class="services-item-top">
              <div class="services-top-left">
                <img src="../assets/img/design.svg" alt="" />
                <span class="services-top-category">Дизайн</span>
              </div>
              <span class="services-top-right">от 9 лет</span>
            </div>
            <h4 class="services-item-title">Графический дизайн</h4>
            <p class="services-item-text">
              сделаем сайты и игры, в которые можно играть с друзьями...
            </p>
            <button class="btn btn__services btn__services__1">
              Подробнее
            </button>
          </div>
        </div>
        <div class="services-item-persp">
          <div class="services-item services-item__2">
            <div class="services-item-top">
              <div class="services-top-left">
                <img src="../assets/img/web.svg" alt="" />
                <span class="services-top-category">Программирование</span>
              </div>
              <span class="services-top-right">от 9 лет</span>
            </div>
            <h4 class="services-item-title">Разработка сайтов</h4>
            <p class="services-item-text">
              сделаем сайты и игры, в которые можно играть с друзьями...
            </p>
            <button class="btn btn__services btn__services__2">
              Подробнее
            </button>
          </div>
        </div>
        <div class="services-item-persp">
          <div class="services-item services-item__3">
            <div class="services-item-top">
              <div class="services-top-left">
                <img src="../assets/img/design.svg" alt="" />
                <span class="services-top-category">Дизайн</span>
              </div>
              <span class="services-top-right">от 9 лет</span>
            </div>
            <h4 class="services-item-title">Вебдизайн</h4>
            <p class="services-item-text">
              сделаем сайты и игры, в которые можно играть с друзьями...
            </p>
            <button class="btn btn__services btn__services__3">
              Подробнее
            </button>
          </div>
        </div>
        <div class="services-item-persp">
          <div class="services-item services-item__4">
            <div class="services-item-top">
              <div class="services-top-left">
                <img src="../assets/img/alg.svg" alt="" />
                <span class="services-top-category">Алгоритмы</span>
              </div>
              <span class="services-top-right">от 9 лет</span>
            </div>
            <h4 class="services-item-title">Игры на Scratch</h4>
            <p class="services-item-text">
              сделаем сайты и игры, в которые можно играть с друзьями...
            </p>
            <button class="btn btn__services btn__services__4">
              Подробнее
            </button>
          </div>
        </div>
        <div class="services-item-persp">
          <div class="services-item services-item__5">
            <div class="services-item-top">
              <div class="services-top-left">
                <img src="../assets/img/web.svg" alt="" />
                <span class="services-top-category">Программирование</span>
              </div>
              <span class="services-top-right">от 9 лет</span>
            </div>
            <h4 class="services-item-title">Java</h4>
            <p class="services-item-text">
              сделаем сайты и игры, в которые можно играть с друзьями...
            </p>
            <button class="btn btn__services btn__services__5">
              Подробнее
            </button>
          </div>
        </div>
        <div class="services-item-persp">
          <div class="services-item services-item__6">
            <div class="services-item-top">
              <div class="services-top-left">
                <img src="../assets/img/web.svg" alt="" />
                <span class="services-top-category">Программирование</span>
              </div>
              <span class="services-top-right">от 9 лет</span>
            </div>
            <h4 class="services-item-title">Python</h4>
            <p class="services-item-text">
              сделаем сайты и игры, в которые можно играть с друзьями...
            </p>
            <button class="btn btn__services btn__services__6">
              Подробнее
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  mounted() {
    const cards = document.querySelectorAll(".services-item-persp");
    console.log(cards.length);
    for (let i = 0; i < cards.length; i++) {
      const card = cards[i];
      card.addEventListener("mousemove", rotate);
      card.addEventListener("mouseout", clearRotate);
    }
    function rotate() {
      const cardItem = this.querySelector(".services-item");
      const halfHeight = cardItem.offsetHeight / 2;
      const halfWidth = cardItem.offsetWidth / 2;

      cardItem.style.transform =
        "rotateX(" +
        -(event.offsetY - halfHeight) / 30 +
        "deg) rotateY(" +
        (event.offsetX - halfWidth) / 30 +
        "deg)";
    }
    function clearRotate() {
      const cardItem = this.querySelector(".services-item");
      cardItem.style.transform =
        "rotate(0)";
    }
  },
  methods: {
    rotate(event) {},
  },
};
</script>