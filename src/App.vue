<template>
  <div class=" min-h-screen bg-linear-to-br from-gray-900 via-blue-900 to-gray-900">

    <Navbar/>
    <Hero/>
    <service/>
    <About/>
    <Experience/>
    <Projects/>
    <Contact/>
    <Testimonial/>

    
  </div>
</template>
<script>

  import {ref,nextTick, onMounted } from 'vue';
  import AOS from 'aos';
  import 'aos/dist/aos.css';
  import Navbar from './components/Navbar.vue'
  import Hero from './components/Hero.vue'
  import Service from './components/Service.vue'
  import About from './components/About.vue'
  import Experience from './components/Experience.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';
import Testimonial from './components/Testimonial.vue';




  export default {
    components: {
      Navbar,
      Hero,
      Service,
      About,
      Experience,
      Projects,
      Contact,
      Testimonial
    },
    setup() {

      const loading =ref(true);
      onMounted(async() => {
        await nextTick();

        AOS.init({
          duration:800,
          once: false,
          offset: 100,
          easing: 'ease-in-out',
        });
        setTimeout(() => {
          loading.value = false;
        },800);
      });
      return{loading};
    }
  }
</script>
<style lang="">
  
</style>





