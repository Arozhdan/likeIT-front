<template>
  <div class="program-page" v-if="!$apollo.loading">
    <header class="program-header">
      <Nav class="program-nav" />
      <div style="z-index: 1500" class="header-body container">
        <div class="header-inner row">
          <div class="header-contnent col-md-7">
            <span class="header-subtitle">Базовый</span>
            <h1 class="header-title">
              {{ programs[0].name }}
              <span class="services-top-right header-title-span"
                >от {{ programs[0].age.num }} лет</span
              >
            </h1>
            <p class="header-suptitle">
              {{ programs[0].description }}
            </p>
            <button class="btn btn__header">Получить консультацию</button>
            <button class="btn btn__header">Начать учиться</button>
            <div class="header-contacts">
              <span class="header-contacts-text"
                >LikeIT school в соц. сетях</span
              >
              <div class="header-contacts-links">
                <svg
                  width="31"
                  height="30"
                  viewBox="0 0 31 30"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <g clip-path="url(#clip0)">
                    <path
                      d="M29.973 8.82008C29.9027 7.22607 29.6449 6.1302 29.2757 5.18061C28.8947 4.17264 28.3087 3.27022 27.5409 2.52002C26.7907 1.75816 25.8823 1.16615 24.886 0.79117C23.9309 0.421912 22.8408 0.16414 21.2468 0.0938599C19.6409 0.0176273 19.131 0 15.058 0C10.9849 0 10.4751 0.0176273 8.87515 0.0879078C7.28114 0.158188 6.18527 0.416188 5.23591 0.785218C4.22772 1.16615 3.32529 1.7522 2.5751 2.52002C1.81324 3.27022 1.22146 4.1786 0.846253 5.17488C0.476995 6.1302 0.219224 7.22011 0.148944 8.81413C0.0727115 10.42 0.0550842 10.9299 0.0550842 15.0029C0.0550842 19.076 0.0727115 19.5858 0.142992 21.1858C0.213272 22.7798 0.471272 23.8757 0.84053 24.8253C1.22146 25.8332 1.81324 26.7356 2.5751 27.4858C3.32529 28.2477 4.23367 28.8397 5.22996 29.2147C6.18527 29.584 7.27519 29.8417 8.86943 29.912C10.4692 29.9825 10.9792 29.9999 15.0523 29.9999C19.1253 29.9999 19.6351 29.9825 21.2351 29.912C22.8291 29.8417 23.925 29.584 24.8743 29.2147C26.8905 28.4352 28.4845 26.8412 29.264 24.8253C29.633 23.8699 29.891 22.7798 29.9613 21.1858C30.0316 19.5858 30.0492 19.076 30.0492 15.0029C30.0492 10.9299 30.0433 10.42 29.973 8.82008ZM27.2714 21.0686C27.2069 22.5337 26.9608 23.3249 26.7557 23.8523C26.2516 25.1593 25.2143 26.1965 23.9074 26.7006C23.3799 26.9057 22.583 27.1518 21.1236 27.2162C19.5413 27.2867 19.0667 27.3041 15.0639 27.3041C11.0612 27.3041 10.5807 27.2867 9.00404 27.2162C7.53891 27.1518 6.74774 26.9057 6.22029 26.7006C5.56991 26.4602 4.97791 26.0793 4.4974 25.5812C3.99925 25.0947 3.61832 24.5086 3.37795 23.8583C3.17283 23.3308 2.92673 22.5337 2.86241 21.0745C2.7919 19.4922 2.7745 19.0174 2.7745 15.0146C2.7745 11.0118 2.7919 10.5313 2.86241 8.95492C2.92673 7.48979 3.17283 6.69862 3.37795 6.17117C3.61832 5.52056 3.99925 4.92879 4.50335 4.44804C4.98959 3.9499 5.57564 3.56896 6.22625 3.32882C6.75369 3.1237 7.55081 2.87761 9.00999 2.81305C10.5923 2.74277 11.0671 2.72514 15.0697 2.72514C19.0784 2.72514 19.553 2.74277 21.1296 2.81305C22.5947 2.87761 23.3859 3.1237 23.9133 3.32882C24.5637 3.56896 25.1557 3.9499 25.6362 4.44804C26.1344 4.93451 26.5153 5.52056 26.7557 6.17117C26.9608 6.69862 27.2069 7.49551 27.2714 8.95492C27.3417 10.5373 27.3593 11.0118 27.3593 15.0146C27.3593 19.0174 27.3417 19.4862 27.2714 21.0686Z"
                      fill="white"
                      fill-opacity="0.6"
                    />
                    <path
                      d="M15.058 7.29635C10.8034 7.29635 7.35144 10.7481 7.35144 15.0029C7.35144 19.2578 10.8034 22.7095 15.058 22.7095C19.3129 22.7095 22.7646 19.2578 22.7646 15.0029C22.7646 10.7481 19.3129 7.29635 15.058 7.29635ZM15.058 20.002C12.2979 20.002 10.059 17.7633 10.059 15.0029C10.059 12.2425 12.2979 10.0039 15.058 10.0039C17.8184 10.0039 20.0571 12.2425 20.0571 15.0029C20.0571 17.7633 17.8184 20.002 15.058 20.002Z"
                      fill="white"
                      fill-opacity="0.6"
                    />
                    <path
                      d="M24.8687 6.99165C24.8687 7.9852 24.0631 8.79079 23.0693 8.79079C22.0758 8.79079 21.2702 7.9852 21.2702 6.99165C21.2702 5.99788 22.0758 5.19251 23.0693 5.19251C24.0631 5.19251 24.8687 5.99788 24.8687 6.99165Z"
                      fill="white"
                      fill-opacity="0.6"
                    />
                  </g>
                  <defs>
                    <clipPath id="clip0">
                      <rect
                        width="30"
                        height="30"
                        fill="white"
                        transform="translate(0.00238037)"
                      />
                    </clipPath>
                  </defs>
                </svg>
                <svg
                  width="31"
                  height="30"
                  viewBox="0 0 31 30"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <g clip-path="url(#clip0)">
                    <path
                      d="M29.7349 21.7089C29.6543 21.5739 29.1555 20.4901 26.7554 18.2624C24.2427 15.9297 24.5802 16.3085 27.6067 12.2751C29.4499 9.81864 30.1868 8.31853 29.9562 7.67723C29.7368 7.06593 28.3811 7.2272 28.3811 7.2272L23.8733 7.25345C23.8733 7.25345 23.5395 7.20844 23.2901 7.35658C23.0482 7.50284 22.8926 7.84037 22.8926 7.84037C22.8926 7.84037 22.1781 9.74176 21.2256 11.3581C19.2173 14.769 18.4129 14.949 18.0847 14.7371C17.3215 14.244 17.5128 12.7532 17.5128 11.6957C17.5128 8.38978 18.0135 7.01155 16.5359 6.65528C16.0446 6.53714 15.6845 6.45839 14.4301 6.44526C12.8212 6.42839 11.458 6.45089 10.6873 6.82779C10.1735 7.07906 9.77786 7.63973 10.0198 7.6716C10.3179 7.71098 10.9929 7.85349 11.3511 8.34103C11.8143 8.9692 11.7974 10.3831 11.7974 10.3831C11.7974 10.3831 12.0637 14.274 11.1767 14.7578C10.5673 15.0897 9.73285 14.4127 7.9421 11.3169C7.02516 9.73238 6.33136 7.97913 6.33136 7.97913C6.33136 7.97913 6.19822 7.65285 5.96008 7.47846C5.67131 7.26657 5.26628 7.19907 5.26628 7.19907L0.979715 7.22532C0.979715 7.22532 0.336543 7.24407 0.100276 7.52347C-0.10974 7.77286 0.0833994 8.28665 0.0833994 8.28665C0.0833994 8.28665 3.43989 16.1379 7.23892 20.0963C10.7248 23.7247 14.6813 23.4865 14.6813 23.4865H16.474C16.474 23.4865 17.0159 23.4265 17.2915 23.1284C17.5466 22.8546 17.5372 22.3408 17.5372 22.3408C17.5372 22.3408 17.5015 19.935 18.6191 19.5806C19.7198 19.2318 21.1337 21.9058 22.6319 22.9352C23.7645 23.7134 24.6252 23.5428 24.6252 23.5428L28.6324 23.4865C28.6324 23.4865 30.7288 23.3571 29.7349 21.7089Z"
                      fill="white"
                      fill-opacity="0.6"
                    />
                  </g>
                  <defs>
                    <clipPath id="clip0">
                      <rect
                        width="30"
                        height="30"
                        fill="white"
                        transform="translate(0.00238037)"
                      />
                    </clipPath>
                  </defs>
                </svg>
              </div>
            </div>
          </div>
          <div class="header-img col-md-5"></div>
        </div>
      </div>
    </header>
    <section class="plan">
      <div class="container">
        <div class="plan-inner">
          <h2 class="section-title">программа курса</h2>
          <div class="plan-section-wrapper">
            <h3 class="plan-section-title">Графический Дизайн. Базовый</h3>
            <div class="plan-section">
              <table class="plan-table">
                <tbody>
                  <tr class="plan-row">
                    <td class="plan-name">Графический Дизайн. Базовый</td>
                    <td class="plan-home">-</td>
                    <td class="plan-seminar">1 практика</td>
                    <td class="plan-lesson">1 урок</td>
                  </tr>
                  <tr class="plan-row">
                    <td class="plan-name">Графический Дизайн. Базовый</td>
                    <td class="plan-home">2 ДЗ</td>
                    <td class="plan-seminar">1 практика</td>
                    <td class="plan-lesson">1 урок</td>
                  </tr>
                  <tr class="plan-row">
                    <td class="plan-name">Графический Дизайн. Базовый</td>
                    <td class="plan-home">5 ДЗ</td>
                    <td class="plan-seminar">1 практика</td>
                    <td class="plan-lesson">1 урок</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>

          <div class="plan-section-wrapper">
            <h3 class="plan-section-title">Графический Дизайн. Продвинутый</h3>
            <div class="plan-section">
              <table class="plan-table">
                <tbody>
                  <tr class="plan-row">
                    <td class="plan-name">Графический Дизайн. Базовый</td>
                    <td class="plan-home">-</td>
                    <td class="plan-seminar">1 практика</td>
                    <td class="plan-lesson">1 урок</td>
                  </tr>
                  <tr class="plan-row">
                    <td class="plan-name">Графический Дизайн. Базовый</td>
                    <td class="plan-home">3 ДЗ</td>
                    <td class="plan-seminar">2 практика</td>
                    <td class="plan-lesson">15 урок</td>
                  </tr>
                  <tr class="plan-row">
                    <td class="plan-name">Графический Дизайн. Базовый</td>
                    <td class="plan-home">2 ДЗ</td>
                    <td class="plan-seminar">12 практика</td>
                    <td class="plan-lesson">11 урок</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="program-expect">
      <div class="container">
        <h2 class="section-title">что вас ждет на курсе?</h2>
        <div class="program-expect-inner row">
          <div class="col-md-4">
            <div class="program-expect-item">
              <div class="program-expect-item-img">
                <img src="../../assets/img/time.svg" alt="" />
              </div>
              <h4 class="program-expect-item-title">24 уроков</h4>
              <h4 class="program-expect-item-suptitle">
                Тут нужно что-нибудь классное
              </h4>
            </div>
          </div>
          <div class="col-md-4">
            <div class="program-expect-item">
              <div class="program-expect-item-img">
                <img src="../../assets/img/book.svg" alt="" />
              </div>
              <h4 class="program-expect-item-title">24 уроков</h4>
              <h4 class="program-expect-item-suptitle">
                Тут нужно что-нибудь классное
              </h4>
            </div>
          </div>

          <div class="col-md-4">
            <div class="program-expect-item">
              <div class="program-expect-item-img">
                <img src="../../assets/img/scheme.svg" alt="" />
              </div>
              <h4 class="program-expect-item-title">24 уроков</h4>
              <h4 class="program-expect-item-suptitle">
                Тут нужно что-нибудь классное
              </h4>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="for-whom">
      <div class="container">
        <h2 class="section-title">что вас ждет на курсе?</h2>
        <p class="section-suptitle">
          В нашем образовательном центре мы предоставляем множество преимуществ
          для успешного обучения ваших детей, помогая при этом развивать их
          аналитически.
        </p>
        <div class="whom-inner row">
          <div class="col-md-3">
            <div class="whom-item">
              <div class="whom-item-img">
                <img src="../../assets/img/set.svg" alt="" />
              </div>
              <p class="whom-item-paragraph">
                Для тех, кто хочет развивать креативность
              </p>
            </div>
          </div>
          <div class="col-md-3">
            <div class="whom-item">
              <div class="whom-item-img">
                <img src="../../assets/img/star.svg" alt="" />
              </div>
              <p class="whom-item-paragraph">
                Для тех, кто хочет развивать креативность
              </p>
            </div>
          </div>
          <div class="col-md-3">
            <div class="whom-item">
              <div class="whom-item-img">
                <img src="../../assets/img/suit.svg" alt="" />
              </div>
              <p class="whom-item-paragraph">
                Для тех, кто хочет развивать креативность
              </p>
            </div>
          </div>
          <div class="col-md-3">
            <div class="whom-item">
              <div class="whom-item-img">
                <img src="../../assets/img/set.svg" alt="" />
              </div>
              <p class="whom-item-paragraph">
                Для тех, кто хочет развивать креативность
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="you-get">
      <div class="you-get-img">
        <img src="../../assets/img/cookie.png" alt="" />
      </div>
      <div class="container">
        <h2 class="section-title">что вы получаете?</h2>
        <div class="you-get-inner">
          <div class="you-get-inner-first row">
            <div class="col-md-4">
              <div class="you-get-item">
                <div class="you-get-item-top you-get-item-top__1"></div>
                <h4 class="you-get-item-title">
                  сложное <br />
                  простыми словами
                </h4>
                <p class="you-get-item-suptitle">
                  Тут нужно что-нибудь классное написать побольше о том. что за
                  ступени отбора такие.
                </p>
              </div>
            </div>
            <div class="col-md-4">
              <div class="you-get-item">
                <div class="you-get-item-top you-get-item-top__2"></div>
                <h4 class="you-get-item-title">
                  5 ступеней <br />
                  отбора Кадров
                </h4>
                <p class="you-get-item-suptitle">
                  Тут нужно что-нибудь классное написать побольше о том. что за
                  ступени отбора такие.
                </p>
              </div>
            </div>
          </div>
          <div class="you-get-inner-second row">
            <div class="col-md-4">
              <div class="you-get-item">
                <div class="you-get-item-top you-get-item-top__3"></div>
                <h4 class="you-get-item-title">
                  Индивидуальный подход к каждому
                </h4>
                <p class="you-get-item-suptitle">
                  Тут нужно что-нибудь классное написать побольше о том. что за
                  ступени отбора такие.
                </p>
              </div>
            </div>
            <div class="col-md-4">
              <div class="you-get-item">
                <div class="you-get-item-top you-get-item-top__4"></div>
                <h4 class="you-get-item-title">
                  Индивидуальный подход к каждому
                </h4>
                <p class="you-get-item-suptitle">
                  Тут нужно что-нибудь классное написать побольше о том. что за
                  ступени отбора такие.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="process">
      <div class="container">
        <h2 class="section-title">Индивидуальные онлайн-уроки</h2>
        <p class="section-suptitle">
          В нашем образовательном центре мы предоставляем множество преимуществ
          для успешного обучения ваших детей, помогая при этом развивать их
          аналитиче
        </p>
        <div class="process-inner row">
          <div class="col-md-3">
            <div class="process-item">
              <div class="process-item-img">
                <img src="../../assets/img/n1.svg" alt="" />
              </div>
              <h4 class="process-item-title">
                Вводная лекция с преподавателем
              </h4>
              <p class="process-item-text">
                Нужен только комютер и доступ к Интернету
              </p>
            </div>
          </div>
          <div class="col-md-3">
            <div class="process-item">
              <div class="process-item-img">
                <img src="../../assets/img/n2.svg" alt="" />
              </div>
              <h4 class="process-item-title">Самостоятельные практики и ДЗ</h4>
              <p class="process-item-text">
                Нужен только комютер и доступ к Интернету
              </p>
            </div>
          </div>
          <div class="col-md-3">
            <div class="process-item">
              <div class="process-item-img">
                <img src="../../assets/img/n3.svg" alt="" />
              </div>
              <h4 class="process-item-title">Разбор ошибок и портфолио</h4>
              <p class="process-item-text">
                Нужен только комютер и доступ к Интернету
              </p>
            </div>
          </div>
          <div class="col-md-3">
            <div class="process-item">
              <div class="process-item-img">
                <img src="../../assets/img/n4.svg" alt="" />
              </div>
              <h4 class="process-item-title">
                Вводная лекция с преподавателем
              </h4>
              <p class="process-item-text">
                Нужен только комютер и доступ к Интернету
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <Testimonials />
    <Pricing />
    <section class="contact">
      <div class="container">
        <div class="contact-inner">
          <div class="contact-left">
            <h2 class="contact-left-title">
              Хотите Начать <br />
              Обучаться с Нами?
            </h2>
            <ul class="contact-left-list">
              <li class="contact-left-list-item">
                Подберем учителя индивидуально с учетом уровня и темперамента
                ученика
              </li>
              <li class="contact-left-list-item">
                Грамотно организуем процесс учебы так, чтобы ребенку
                действительно нравилось то, что он изучает
              </li>
              <li class="contact-left-list-item">
                На вводном занятии познакомим Вас с репетитором и составим план
                обучения
              </li>
            </ul>
          </div>
          <div class="contact-right">
            <div class="contact-right-img">
              <img src="../../assets/img/call.svg" alt="" />
            </div>
            <h3 class="contact-right-title">
              Начните свой путь в LikeIT уже сегодня!
            </h3>
            <p class="contact-right-text">
              Запишитесь на пробное занятие и дай своему ребенку возможность
              обучиться профессиям будущего.
            </p>
            <button class="btn btn__plank">Получить консультацию</button>
            <button class="btn btn__plank btn__plank-empty">
              Написать нам
            </button>
          </div>
        </div>
      </div>
    </section>
    <Footer />
  </div>
  <div class="loader" v-else >
    <h1>LOADING THE PAGE</h1>
  </div>
</template>
<script>
import programQuery from "../../apollo/queries/program/program.gql";
import Testimonials from "@/components/Testimonials.vue";
import Pricing from "@/components/Pricing.vue";
import Footer from "@/components/Footer.vue";
import Nav from "@/components/Nav.vue";
export default {
  data() {
    return {
      programs:{},
      api_url: process.env.strapiBaseUri,
    };
  },
  apollo: {
    programs: {
      prefetch: true,
      query: programQuery,
      variables() {
        return { slug: this.$route.params.slug };
      },
    },
  },
  components: {
    Nav,
    Testimonials,
    Pricing,
    Footer,
  },
};
</script>