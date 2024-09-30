<template>
  <header class="bg-primary-600 shadow-lg">
    <div class="container mx-auto px-4">
      <div class="flex items-center justify-between py-6">
        <router-link
          to="/"
          class="text-2xl font-bold text-white hover:text-primary-200 transition duration-300"
        >
          Zeko Rent
        </router-link>
        <nav class="hidden md:flex space-x-6">
          <router-link
            v-for="item in menuItems"
            :key="item.path"
            :to="item.path"
            class="text-white hover:text-primary-200 transition duration-300"
          >
            {{ item.name }}
          </router-link>
        </nav>
        <button
          @click="toggleMenu"
          class="md:hidden text-white focus:outline-none"
        >
          <svg
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              v-if="!isMenuOpen"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h16"
            />
            <path
              v-else
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M6 18L18 6M6 6l12 12"
            />
          </svg>
        </button>
      </div>
    </div>
    <div v-show="isMenuOpen" class="md:hidden">
      <nav class="px-4 pt-2 pb-4 space-y-2">
        <router-link
          v-for="item in menuItems"
          :key="item.path"
          :to="item.path"
          class="block text-white hover:text-primary-200 transition duration-300"
          @click="closeMenu"
        >
          {{ item.name }}
        </router-link>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isMenuOpen: false,
      menuItems: [
        { name: "Home", path: "/" },
        { name: "Services", path: "/services" },
        { name: "About", path: "/about" },
        { name: "Contact", path: "/contact" },
      ],
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    closeMenu() {
      this.isMenuOpen = false;
    },
  },
};
</script>

<style scoped>
@media (max-width: 1023px) {
  nav {
    position: absolute;
    left: 0;
    right: 0;
    top: 100%;
    background-color: #2563eb; /* blue-600 */
    box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1),
      0 2px 4px -1px rgba(0, 0, 0, 0.06);
  }
  nav ul {
    padding: 1rem;
  }
  nav ul li {
    margin-bottom: 0.75rem;
  }
}
</style>
