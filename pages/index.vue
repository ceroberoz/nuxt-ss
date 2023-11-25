<template>
  <div class="container">
    <Logo />
    <TextInputSection />
    <Footer />
  </div>
</template>

<script>
import Logo from '@/components/Logo.vue'
import TextInputSection from '@/components/TextInputSection.vue'
import Footer from '@/components/Footer.vue'

export default {
  components: {
    Logo,
    TextInputSection,
    Footer,
  },
}
</script>

<style>
.container {
  /* Your container styles here */
  background-color: #f6f6f6;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15);
  border-radius: 8px;

  width: 100vw;
}
</style>