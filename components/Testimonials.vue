<template>
  <section tag="section" class="testimonials">
    <div class="container">
      <h2 class="section-title">Отзывы</h2>
      <p class="section-suptitle">
        Те самые люди, которые позволяют нам быть теми, кем мы являемся!
      </p>
      <carousel
        class="testimonials-slider"
        :navigation-enabled="true"
        :navigation-next-label="nextLabel"
        :navigation-prev-label="prevLabel"
        :paginationEnabled="false"
      >
        <slide class="testimonial-item-container">
          <div class="testimonial-item">
            <div class="testimonials-top">
              <div class="testiomonial-rating">
                <img src="../assets/img/stars.svg" alt="" />
              </div>
              <span class="date">2 дня назад</span>
            </div>
            <p class="testimonial-body">
              “ Дочка с огромным удовольствием занимается с Эдуардом. Я думала,
              что её разочарует отсутствие компании сверстников, но ничего
              подобного нет и в помине. После каждого урока с радостью
              показывает мне, то что сделали за урок. Спасибо! ”
            </p>
            <div class="testimonial-bottom">
              <div class="testimonials-author">
                <div class="testimonial-author-img">
                  <img src="../assets/img/avatar.svg" alt="">
                </div>
                <span class="testimonial-author-name">Марина Кравец </span>
              </div>
              <div class="tesimonaials-link">
                <img src="../assets/img/vk2.svg" alt="" />
              </div>
            </div>
          </div>
        </slide>
       <slide class="testimonial-item-container">
          <div class="testimonial-item">
            <div class="testimonials-top">
              <div class="testiomonial-rating">
                <img src="../assets/img/stars.svg" alt="" />
              </div>
              <span class="date">2 дня назад</span>
            </div>
            <p class="testimonial-body">
              “ Дочка с огромным удовольствием занимается с Эдуардом. Я думала,
              что её разочарует отсутствие компании сверстников, но ничего
              подобного нет и в помине. После каждого урока с радостью
              показывает мне, то что сделали за урок. Спасибо! ”
            </p>
            <div class="testimonial-bottom">
              <div class="testimonials-author">
                <div class="testimonial-author-img">
                  <img src="../assets/img/avatar.svg" alt="">
                </div>
                <span class="testimonial-author-name">Марина Кравец </span>
              </div>
              <div class="tesimonaials-link">
                <img src="../assets/img/vk2.svg" alt="" />
              </div>
            </div>
          </div>
        </slide>
        <slide class="testimonial-item-container">
          <div class="testimonial-item">
            <div class="testimonials-top">
              <div class="testiomonial-rating">
                <img src="../assets/img/stars.svg" alt="" />
              </div>
              <span class="date">2 дня назад</span>
            </div>
            <p class="testimonial-body">
              “ Дочка с огромным удовольствием занимается с Эдуардом. Я думала,
              что её разочарует отсутствие компании сверстников, но ничего
              подобного нет и в помине. После каждого урока с радостью
              показывает мне, то что сделали за урок. Спасибо! ”
            </p>
            <div class="testimonial-bottom">
              <div class="testimonials-author">
                <div class="testimonial-author-img">
                  <img src="../assets/img/avatar.svg" alt="">
                </div>
                <span class="testimonial-author-name">Марина Кравец </span>
              </div>
              <div class="tesimonaials-link">
                <img src="../assets/img/vk2.svg" alt="" />
              </div>
            </div>
          </div>
        </slide>
        <slide class="testimonial-item-container">
          <div class="testimonial-item">
            <div class="testimonials-top">
              <div class="testiomonial-rating">
                <img src="../assets/img/stars.svg" alt="" />
              </div>
              <span class="date">2 дня назад</span>
            </div>
            <p class="testimonial-body">
              “ Дочка с огромным удовольствием занимается с Эдуардом. Я думала,
              что её разочарует отсутствие компании сверстников, но ничего
              подобного нет и в помине. После каждого урока с радостью
              показывает мне, то что сделали за урок. Спасибо! ”
            </p>
            <div class="testimonial-bottom">
              <div class="testimonials-author">
                <div class="testimonial-author-img">
                  <img src="../assets/img/avatar.svg" alt="">
                </div>
                <span class="testimonial-author-name">Марина Кравец </span>
              </div>
              <div class="tesimonaials-link">
                <img src="../assets/img/vk2.svg" alt="" />
              </div>
            </div>
          </div>
        </slide>
      </carousel>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      nextLabel: "<div class='slide-arr slide-arr__next'></div>",
      prevLabel: "<div class='slide-arr slide-arr__prev'></div>",
    };
  },
};
</script>