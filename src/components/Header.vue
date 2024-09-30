<template>
  <header class="bg-blue-600 shadow-md">
    <div class="container mx-auto px-4">
      <div class="flex flex-wrap items-center justify-between py-6">
        <!-- Logo -->
        <div class="flex items-center flex-shrink-0 mr-6">
          <router-link to="/" class="font-bold text-2xl text-white">
            Zeko Rent
          </router-link>
        </div>

        <!-- Mobile menu button -->
        <div class="block lg:hidden">
          <button
            @click="toggleMenu"
            class="flex items-center px-3 py-2 border rounded text-white border-white hover:text-blue-200 hover:border-blue-200"
          >
            <svg
              class="fill-current h-4 w-4"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
            </svg>
          </button>
        </div>

        <!-- Navigation Menu -->
        <nav
          :class="{ hidden: !isMenuOpen, block: isMenuOpen }"
          class="w-full lg:flex lg:items-center lg:w-auto"
        >
          <ul class="text-lg lg:flex-grow">
            <li
              v-for="(item, index) in menuItems"
              :key="index"
              class="block mt-4 lg:inline-block lg:mt-0 mr-6"
            >
              <router-link
                :to="item.path"
                class="text-white hover:text-blue-200 transition duration-300"
                @click="closeMenu"
              >
                {{ item.name }}
              </router-link>
            </li>
          </ul>
        </nav>
      </div>
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
