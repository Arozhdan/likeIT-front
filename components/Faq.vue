<template>
  <section class="faq">
    <div class="container">
      <h2 class="section-title">Что мы Вам даем?</h2>
      <p class="section-suptitle">
        В нашем образовательном центре мы предоставляем множество преимуществ
        для успешного обучения ваших детей, помогая при этом развивать их
        аналитический склад ума, тврочество и поддерживая интерес.
      </p>
      <div class="faq-collapses">
        <v-collapse-group :onlyOneActive="false">
          <div class="faq-collapse" v-for="faq in faqs" :key="faq.id">
            <v-collapse-wrapper>
              <div class="faq-item-header-wrapper" v-collapse-toggle>
                <h4 class="faq-item-header">
                  {{ faq.question }}
                </h4>
              </div>
              <div
                class="faq-item-body v-collapse-content-end"
                v-collapse-content
              >
                <p class="faq-item-body-text">
                  {{ faq.answer }}
                </p>
                <img
                  src="../assets/img/down-arrow.svg"
                  alt=""
                  class="faq-collapse-img"
                />
              </div>
            </v-collapse-wrapper>
          </div>
        </v-collapse-group>
      </div>
    </div>
  </section>
</template>
<script>
import faqQuery from "../apollo/queries/faq/faq.gql";
export default {
  data() {
    return {
      faqs: {},
    };
  },
  apollo: {
    faqs: {
      prefetch: true,
      query: faqQuery,
    },
  },
  data: function () {
    return {};
  },
};
</script>