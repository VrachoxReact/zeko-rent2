<template>
  <div class="contact">
    <div class="container mx-auto px-4 py-12">
      <h1 class="text-4xl font-bold text-center mb-8">Contact Us</h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-12">
        <!-- Contact Form -->
        <div class="bg-white rounded-lg shadow-md p-6">
          <h2 class="text-2xl font-semibold mb-4">Get in Touch</h2>
          <form @submit.prevent="submitForm">
            <div class="mb-4">
              <label for="name" class="block text-gray-700 font-bold mb-2"
                >Name</label
              >
              <input
                type="text"
                id="name"
                v-model="form.name"
                required
                class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
              />
            </div>
            <div class="mb-4">
              <label for="email" class="block text-gray-700 font-bold mb-2"
                >Email</label
              >
              <input
                type="email"
                id="email"
                v-model="form.email"
                required
                class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
              />
            </div>
            <div class="mb-4">
              <label for="message" class="block text-gray-700 font-bold mb-2"
                >Message</label
              >
              <textarea
                id="message"
                v-model="form.message"
                required
                rows="4"
                class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500"
              ></textarea>
            </div>
            <button
              type="submit"
              class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded-full"
            >
              Send Message
            </button>
          </form>
        </div>

        <!-- Contact Information and Map -->
        <div>
          <div class="bg-white rounded-lg shadow-md p-6 mb-6">
            <h2 class="text-2xl font-semibold mb-4">Contact Information</h2>
            <ul class="space-y-2">
              <li class="flex items-center">
                <i class="fas fa-map-marker-alt text-blue-500 mr-2"></i>
                123 Rental Street, City, Country
              </li>
              <li class="flex items-center">
                <i class="fas fa-phone text-blue-500 mr-2"></i>
                +1 (123) 456-7890
              </li>
              <li class="flex items-center">
                <i class="fas fa-envelope text-blue-500 mr-2"></i>
                info@zekorent.com
              </li>
            </ul>
          </div>
          <div class="bg-white rounded-lg shadow-md p-6">
            <h2 class="text-2xl font-semibold mb-4">Our Location</h2>
            <!-- Replace the img tag with an actual map component or embed a Google Maps iframe here -->
            <img
              src="https://placehold.co/600x300/png?text=Map"
              alt="Zeko Rent Location"
              class="w-full rounded-lg"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactView",
  data() {
    return {
      form: {
        name: "",
        email: "",
        message: "",
      },
    };
  },
  methods: {
    submitForm() {
      // Here you would typically send the form data to your backend
      console.log("Form submitted:", this.form);
      // Reset form after submission
      this.form = { name: "", email: "", message: "" };
      // You could also show a success message to the user here
    },
  },
};
</script>

<script setup>
// This is needed to use Font Awesome icons
import "@fortawesome/fontawesome-free/css/all.css";
</script>
