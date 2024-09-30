<template>
  <div class="about">
    <div class="container mx-auto px-4 py-12">
      <h1 class="text-4xl font-bold text-center mb-8">About Zeko Rent</h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-12 items-center mb-16">
        <div>
          <img
            src="https://placehold.co/600x400/png?text=Zeko+Rent+Team"
            alt="Zeko Rent Team"
            class="rounded-lg shadow-lg w-full"
          />
        </div>
        <div>
          <h2 class="text-2xl font-semibold mb-4">Our Mission</h2>
          <p class="text-gray-700 mb-4">
            At Zeko Rent, our mission is to revolutionize the rental experience
            by connecting property owners with quality tenants through
            innovative technology and exceptional service. We strive to make the
            rental process seamless, transparent, and enjoyable for all parties
            involved.
          </p>
          <p class="text-gray-700">
            Since our founding in 2010, we've helped thousands of people find
            their perfect homes and assisted property owners in maximizing the
            value of their investments.
          </p>
        </div>
      </div>

      <div class="bg-gray-100 rounded-lg p-8 mb-16">
        <h2 class="text-2xl font-semibold mb-6 text-center">
          Why Choose Zeko Rent?
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
          <div class="text-center">
            <div class="text-4xl font-bold text-blue-500 mb-2">10+</div>
            <div class="text-gray-700">Years of Experience</div>
          </div>
          <div class="text-center">
            <div class="text-4xl font-bold text-blue-500 mb-2">50,000+</div>
            <div class="text-gray-700">Happy Tenants</div>
          </div>
          <div class="text-center">
            <div class="text-4xl font-bold text-blue-500 mb-2">98%</div>
            <div class="text-gray-700">Customer Satisfaction</div>
          </div>
        </div>
      </div>

      <div class="mb-16">
        <h2 class="text-2xl font-semibold mb-6">Our Values</h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
          <div>
            <h3 class="text-xl font-semibold mb-2">Transparency</h3>
            <p class="text-gray-700">
              We believe in open and honest communication with all our clients,
              ensuring a trustworthy rental experience.
            </p>
          </div>
          <div>
            <h3 class="text-xl font-semibold mb-2">Innovation</h3>
            <p class="text-gray-700">
              We continuously improve our technology and processes to provide
              the best possible service to our users.
            </p>
          </div>
          <div>
            <h3 class="text-xl font-semibold mb-2">Customer-Centric</h3>
            <p class="text-gray-700">
              Our clients' needs are at the heart of everything we do, driving
              us to exceed expectations.
            </p>
          </div>
          <div>
            <h3 class="text-xl font-semibold mb-2">Integrity</h3>
            <p class="text-gray-700">
              We uphold the highest ethical standards in all our business
              practices and relationships.
            </p>
          </div>
        </div>
      </div>

      <div class="text-center">
        <h2 class="text-2xl font-semibold mb-4">Ready to Get Started?</h2>
        <p class="text-gray-700 mb-6">
          Join thousands of satisfied tenants and property owners who trust Zeko
          Rent.
        </p>
        <button
          class="bg-blue-500 hover:bg-blue-600 text-white font-bold py-2 px-6 rounded-full text-lg"
        >
          Explore Properties
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AboutView",
};
</script>
