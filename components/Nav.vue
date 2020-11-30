
<template>
  <nav class="nav">
    <div class="container">
      <div class="row justify-content-between nav-wrapper">
        <nuxt-link class="logo col-md-2" to="/" tag="div">
          <img src="../assets/img/logo.svg" alt="" />
        </nuxt-link>
        <div class="nav-links col-lg-9 col-md-10 row justify-content-between">
          <nuxt-link tag="a" to="/" class="nav-link"> Главная</nuxt-link>
          <nuxt-link tag="a" to="/#about" class="nav-link">О Нас</nuxt-link>
          <div class="nav-links-prg">
            <nuxt-link tag="a" to="/#programs" class="nav-link"
              >Программы <img src="../assets/img/prog-arr.svg" alt="" />
            </nuxt-link>
            <div class="nav-prog-menu">
              <div
                class="nav-center-item"
                v-for="category in categories"
                :key="category.id"
              >
                <div class="nav-center-item-title">
                  <img :src="api_url + category.navimage.url" alt="" />
                  <span>{{ category.name }}</span>
                </div>
                <ul class="nav-center-item-list">
                  <nuxt-link
                    tag="li"
                    :to="'/programs/' + program.slug"
                    v-for="program in category.programs"
                    :key="program.id"
                  >
                    {{ program.name }}
                  </nuxt-link>
                </ul>
              </div>
            </div>
          </div>
          <nuxt-link tag="a" to="/#pricing" class="nav-link">Тарифы</nuxt-link>
          <nuxt-link tag="a" to="/#testimonials" class="nav-link"
            >Отзывы</nuxt-link
          >
          <nuxt-link tag="a" to="/#contacts" class="nav-link"
            >Контакты</nuxt-link
          >
          <nuxt-link tag="a" to="/#faq" class="nav-link">FAQ</nuxt-link>
          <a :href="'tel:' + links[0].phone" class="btn btn__nav">{{
            links[0].phone
          }}</a>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>
import linksQuery from "../apollo/queries/link/links.gql";
import categoriesQuery from "../apollo/queries/category/categoriesMenu.gql";
export default {
  data() {
    return {
      api_url: process.env.strapiBaseUri,
      links: {},
      categories: {},
    };
  },
  apollo: {
    links: {
      prefetch: true,
      query: linksQuery,
    },
    categories: {
      prefetch: true,
      query: categoriesQuery,
    },
  },
};
</script>