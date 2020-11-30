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
        <slide
          class="testimonial-item-container"
          v-for="testimonial in testimonials"
          :key="testimonial.id"
        >
          <div class="testimonial-item">
            <div class="testimonials-top">
              <div class="testiomonial-rating">
                <img src="../assets/img/stars.svg" alt="" />
              </div>
              <span class="date">2 дня назад</span>
            </div>
            <p class="testimonial-body">“ {{ testimonial.text }} ”</p>
            <div class="testimonial-bottom">
              <div class="testimonials-author">
                <div class="testimonial-author-img">
                  <img
                    :src="api_url + testimonial.avatar.url"
                    alt=""
                    v-if="testimonial.avatar"
                  />
                  <img
                    src="../assets/img/avatar.svg"
                    class="testimonial-author-img-placeholder"
                    alt=""
                    v-else
                  />
                </div>
                <span class="testimonial-author-name">{{
                  testimonial.author
                }}</span>
              </div>
              <div class="tesimonaials-link">
                <a
                  v-if="testimonial.link"
                  :href="testimonial.link"
                  target="_blank"
                  rel="noopener noreferrer"
                >
                  <img src="../assets/img/vk2.svg" alt="" />
                </a>
              </div>
            </div>
          </div>
        </slide>
      </carousel>
    </div>
  </section>
</template>
<script>
import testimonialsQuery from "../apollo/queries/testimonial/testimonails.gql";
export default {
  data() {
    return {
      nextLabel: "<div class='slide-arr slide-arr__next'></div>",
      prevLabel: "<div class='slide-arr slide-arr__prev'></div>",
      testimonials: {},
      api_url: process.env.strapiBaseUri,
    };
  },
  apollo: {
    testimonials: {
      prefetch: true,
      query: testimonialsQuery,
    },
  },
};
</script>