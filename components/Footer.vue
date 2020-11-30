<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-inner row">
        <div class="footer-left col-md-3">
          <nuxt-link to="/#">
            <div class="logo">
              <img src="../assets/img/logo.svg" alt="" />
            </div>
          </nuxt-link>
          <span class="header-subtitle footer-suptitle"
            >Онлайн-школа <br />
            информационных технологий</span
          >
          <div class="footer-left-contacts">
            <p>{{links[0].phone}}</p>
            <span>по России бесплатно</span>

            <div class="footer-left-contacts-hot">
              <img src="../assets/img/hot.svg" alt="" />
              <a class="footer-left-contacts-hot-link" href="#"
                >Горячая линия</a
              >
            </div>
            <div class="footer-left-contacts-links">
              <div class="footer-left-contacts-links-email">
                <a href="mailto:info@likeitschool.ru">{{links[0].email}}</a>
              </div>
              <div class="footer-left-contacts-links-icons">
                <a :href="links[0].telegram" target="_blank">
                  <img src="../assets/img/teleg.svg" alt="telegram" />
                </a>
                <a :href="links[0].whatsapp" target="_blank">
                  <img src="../assets/img/wp.svg" alt="telegram" />
                </a>
                <a :href="links[0].vk" target="_blank">
                  <img src="../assets/img/vk.svg" alt="telegram" />
                </a>
                <a :href="links[0].instagram" target="_blank">
                  <img src="../assets/img/inst.svg" alt="telegram" />
                </a>
              </div>
            </div>
          </div>
        </div>
        <div class="footer-spacer col-md-2"></div>
        <div class="footer-center col-md-5">
          <span class="footer-center-title">Программы</span>
          <div class="footer-center-items">
            <div
              class="footer-center-item"
              v-for="category in categories"
              :key="category.id"
            >
              <span class="footer-center-item-title">{{ category.name }}</span>
              <ul class="footer-center-item-list">
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
        <ul class="footer-right col-md-2">
          <li><nuxt-link to="/">Главная </nuxt-link></li>
          <li><nuxt-link to="/#about">О нас </nuxt-link></li>
          <li><nuxt-link to="/#pricing">Тарифы </nuxt-link></li>
          <li><nuxt-link to="/#testimonials">Отзывы </nuxt-link></li>
          <li><nuxt-link to="/#faq">FAQ </nuxt-link></li>
        </ul>
      </div>
    </div>
  </footer>
</template>
<script>
import categoriesQuery from "../apollo/queries/category/categoriesMenu.gql";
import linksQuery from "../apollo/queries/link/links.gql";

export default {
  data() {
    return {
      categories: {},
      links: {},
    };
  },
  apollo: {
    categories: {
      prefetch: true,
      query: categoriesQuery,
    },
    links: {
      prefetch: true,
      query: linksQuery,
    },
  },
};
</script>