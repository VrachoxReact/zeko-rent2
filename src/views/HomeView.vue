<template>
  <div class="home">
    <!-- Hero Section -->
    <section class="hero bg-gray-100 py-20">
      <div
        class="container mx-auto px-4 flex flex-col md:flex-row items-center"
      >
        <div class="md:w-1/2 mb-8 md:mb-0">
          <h1 class="text-4xl md:text-5xl font-bold mb-4">
            Find Your Perfect Rental Property
          </h1>
          <p class="text-xl mb-6">
            Discover a wide range of quality rental properties with Zeko Rent.
          </p>
          <button
            class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded"
          >
            Start Your Search
          </button>
        </div>
        <div class="md:w-1/2">
          <img
            src="https://placehold.co/600x400/png?text=Rental+Property"
            alt="Rental Property"
            class="rounded-lg shadow-lg w-full"
          />
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section class="testimonials py-16">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12">
          What Our Clients Say
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div
            v-for="(testimonial, index) in testimonials"
            :key="index"
            class="bg-white p-6 rounded-lg shadow-md"
          >
            <img
              :src="testimonial.image"
              :alt="testimonial.name"
              class="w-24 h-24 rounded-full mx-auto mb-4"
            />
            <h3 class="text-xl font-semibold text-center mb-2">
              {{ testimonial.name }}
            </h3>
            <p class="text-gray-600 text-center">{{ testimonial.review }}</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Banner -->
    <section class="cta-banner bg-blue-500 py-12">
      <div class="container mx-auto px-4 text-center">
        <h2 class="text-3xl font-bold text-white mb-4">
          Ready to Find Your New Home?
        </h2>
        <p class="text-xl text-white mb-6">
          Browse our extensive list of properties and find the perfect match for
          you.
        </p>
        <button
          class="bg-white text-blue-500 hover:bg-gray-100 font-bold py-2 px-4 rounded"
        >
          View Properties
        </button>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      testimonials: [
        {
          name: "John Doe",
          image: "https://placehold.co/150x150/png?text=John+Doe",
          review:
            "Zeko Rent made finding my dream apartment a breeze. Their service is top-notch!",
        },
        {
          name: "Jane Smith",
          image: "https://placehold.co/150x150/png?text=Jane+Smith",
          review:
            "I've been using Zeko Rent for years. They always have the best properties available.",
        },
        {
          name: "Mike Johnson",
          image: "https://placehold.co/150x150/png?text=Mike+Johnson",
          review:
            "The team at Zeko Rent is professional and responsive. Highly recommended!",
        },
      ],
    };
  },
};
</script>
