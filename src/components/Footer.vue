<template>
  <footer class="bg-secondary-800 text-white">
    <div class="container mx-auto px-4 py-12">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
        <!-- Company Info -->
        <div class="w-full md:w-1/4 mb-6 md:mb-0">
          <h3 class="text-xl font-bold mb-4">Zeko Rent</h3>
          <p class="mb-4">
            Your trusted partner in finding the perfect rental property.
          </p>
          <div class="flex space-x-4">
            <font-awesome-icon :icon="['fab', 'facebook-f']" />
            <font-awesome-icon :icon="['fab', 'twitter']" />
            <font-awesome-icon :icon="['fab', 'instagram']" />
            <font-awesome-icon :icon="['fab', 'linkedin-in']" />
          </div>
        </div>

        <!-- Quick Links -->
        <div class="w-full md:w-1/4 mb-6 md:mb-0">
          <h3 class="text-xl font-bold mb-4">Quick Links</h3>
          <ul class="space-y-2">
            <li v-for="(item, index) in menuItems" :key="index">
              <router-link
                :to="item.path"
                class="hover:text-blue-200 transition duration-300"
              >
                {{ item.name }}
              </router-link>
            </li>
          </ul>
        </div>

        <!-- Services -->
        <div class="w-full md:w-1/4 mb-6 md:mb-0">
          <h3 class="text-xl font-bold mb-4">Our Services</h3>
          <ul class="space-y-2">
            <li>
              <a href="#" class="hover:text-blue-200 transition duration-300"
                >Apartment Rentals</a
              >
            </li>
            <li>
              <a href="#" class="hover:text-blue-200 transition duration-300"
                >House Rentals</a
              >
            </li>
            <li>
              <a href="#" class="hover:text-blue-200 transition duration-300"
                >Commercial Properties</a
              >
            </li>
            <li>
              <a href="#" class="hover:text-blue-200 transition duration-300"
                >Property Management</a
              >
            </li>
          </ul>
        </div>

        <!-- Contact Info -->
        <div class="w-full md:w-1/4">
          <h3 class="text-xl font-bold mb-4">Contact Us</h3>
          <ul class="space-y-2">
            <li class="flex items-center">
              <i class="fas fa-map-marker-alt mr-2"></i>
              123 Rental Street, City, Country
            </li>
            <li class="flex items-center">
              <i class="fas fa-phone mr-2"></i>
              +1 (123) 456-7890
            </li>
            <li class="flex items-center">
              <i class="fas fa-envelope mr-2"></i>
              info@zekorent.com
            </li>
          </ul>
        </div>
      </div>

      <!-- Copyright -->
      <div
        class="border-t border-secondary-700 mt-8 pt-8 text-center text-secondary-400"
      >
        <p>
          &copy; {{ new Date().getFullYear() }} Zeko Rent. All rights reserved.
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";

export default {
  components: {
    FontAwesomeIcon,
  },
  name: "Footer",
  data() {
    return {
      menuItems: [
        { name: "Home", path: "/" },
        { name: "Services", path: "/services" },
        { name: "About", path: "/about" },
        { name: "Contact", path: "/contact" },
      ],
    };
  },
};
</script>

<script setup>
// This is needed to use Font Awesome icons
import "@fortawesome/fontawesome-free/css/all.css";
</script>
