<template>
  <div class="flex flex-col min-h-screen">
    <Header />
    <main class="flex-grow container mx-auto px-4 py-8">
      <router-view></router-view>
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
  },
};
</script>

<style scoped></style>
