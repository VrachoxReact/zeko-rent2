<template>
  <div class="services">
    <h1 class="text-3xl font-bold mb-8 text-center">Our Services</h1>
    <div class="container mx-auto px-4">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="(service, index) in services"
          :key="index"
          class="bg-white rounded-lg shadow-md overflow-hidden"
        >
          <img
            :src="service.image"
            :alt="service.title"
            class="w-full h-48 object-cover"
            loading="lazy"
          />
          <div class="p-6">
            <h2 class="text-xl font-semibold mb-2">{{ service.title }}</h2>
            <p class="text-gray-600 mb-4">{{ service.description }}</p>
            <button
              class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-4 rounded"
            >
              Rent Service
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServicesView",
  data() {
    return {
      services: [
        {
          title: "Apartment Rentals",
          description:
            "Find your perfect apartment in prime locations across the city.",
          image: "https://placehold.co/600x400/png?text=Apartment+Rentals",
        },
        {
          title: "House Rentals",
          description:
            "Discover spacious houses for rent, ideal for families and groups.",
          image: "https://placehold.co/600x400/png?text=House+Rentals",
        },
        {
          title: "Commercial Properties",
          description:
            "Lease office spaces and retail locations for your business needs.",
          image: "https://placehold.co/600x400/png?text=Commercial+Properties",
        },
        {
          title: "Property Management",
          description:
            "Let us handle the day-to-day operations of your rental properties.",
          image: "https://placehold.co/600x400/png?text=Property+Management",
        },
        {
          title: "Tenant Screening",
          description: "Comprehensive background checks for potential tenants.",
          image: "https://placehold.co/600x400/png?text=Tenant+Screening",
        },
        {
          title: "Maintenance Services",
          description:
            "24/7 maintenance support for all your rental properties.",
          image: "https://placehold.co/600x400/png?text=Maintenance+Services",
        },
      ],
    };
  },
};
</script>
