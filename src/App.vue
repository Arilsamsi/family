<template>
  <div id="app">
    <Header />
    <HeroSection />
    <WishList />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import HeroSection from './components/HeroSection.vue';
import Footer from './components/Footer.vue';
import WishList from './components/WishList.vue';

export default {
  components: {
    Header,
    HeroSection,
    WishList,
    Footer,
  },
};
</script>

<style>
body {
  font-family: 'Arial', sans-serif;
  background-color: #f8f4f1;
  margin: 0;
}
</style>
