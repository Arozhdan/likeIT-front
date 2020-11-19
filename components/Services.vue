<template>
  <section class="services">
    <div class="container">
      <h2 class="secondary-title">Программы и курсы LikeIT school</h2>
      <div class="row services-wrapper">
        <div
          class="services-item-persp"
          v-for="program in programs"
          :key="program.id"
        >
          <div class="services-item services-item__1">
            <div class="services-item-top">
              <div class="services-top-left">
                <img src="../assets/img/design.svg" alt="" />
                <span class="services-top-category">{{
                  program.category.name
                }}</span>
              </div>
              <span class="services-top-right"
                >от {{ program.age.num }} лет</span
              >
            </div>
            <h4 class="services-item-title">{{ program.name }}</h4>
            <p class="services-item-text">
              {{ program.description }}
            </p>
            <nuxt-link
              tag="button"
              :to="'/programs/' + program.slug"
              class="btn btn__services btn__services__1"
            >
              Подробнее
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import programsQuery from "../apollo/queries/program/programs.gql";

export default {
  data() {
    return {
      api_url: process.env.strapiBaseUri,
      programs: [],
    };
  },
  apollo: {
    programs: {
      prefetch: true,
      query: programsQuery,
    },
  },
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
      cardItem.style.transform = "rotate(0)";
    }
  },
  methods: {
    rotate(event) {},
  },
};
</script>