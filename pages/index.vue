import { Plank, Teachers, Whyus, Contactus, Faq, Promo } from '../.nuxt/components';
<template>
  <div class="home-page">
    <Header />
    <Advantages />
    <Benefits />
    <Wellcome />
    <About />
    <Services />
    <Plank />
    <Teachers />
    <Whyus />
    <Pricing />
    <Testimonials/>
    <Contactus />
    <Faq/>
    <Promo />
    <Form/>
    <Footer/>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Advantages from "@/components/Advantages.vue";
import Benefits from "@/components/Benefits.vue";
import Wellcome from "@/components/Wellcome.vue";
import About from "@/components/About.vue";
import Services from "@/components/Services.vue";
import Plank from "@/components/Plank.vue";
import Teachers from "@/components/Teachers.vue";
import Whyus from "@/components/Whyus.vue";
import Pricing from "@/components/Pricing.vue";
import Testimonials from "@/components/Testimonials.vue";
import Contactus from "@/components/Contactus.vue"
import Faq from "@/components/Faq.vue"
import Promo from "@/components/Promo.vue"
import Form from "@/components/Form.vue"
import Footer from "@/components/Footer.vue"


export default {
  components: {
    Header,
    Advantages,
    Benefits,
    Wellcome,
    About,
    Services,
    Plank,
    Teachers,
    Whyus,
    Pricing,
    Testimonials,
    Contactus,
    Faq,
    Promo,
    Form,
    Footer
  },
};
</script>



