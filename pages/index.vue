import { Plank, Teachers, Whyus } from '../.nuxt/components';
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
  },
};
</script>



