<template>
  <section
    class="px-6 py-24 xl:px-16 flex justify-center bg-gradient-to-b from-brand-950 to-brand-900"
  >
    <!-- Container -->
    <div
      class="flex flex-col max-w-7xl justify-start md:justify-center items-center w-full"
    >
      <!-- Texts -->
      <div
        class="flex flex-col justify-start md:justify-center items-center max-w-4xl"
      >
        <!-- Quote -->
        <h3 class="text-white md:text-center text-base sm:text-xl md:text-2xl">
          {{ quote }}
        </h3>
        <div class="grid mt-10 gap-4 w-full md:place-items-center">
          <Avatar
            :image="image"
            class="w-16 h-16"
            size="xlarge"
            shape="circle"
          />
          <p
            class="md:text-xl max-w-md w-full md:text-center font-medium text-white"
          >
            {{ client }}
          </p>
          <p class="md:text-xl max-w-md w-full md:text-center text-base text-white/70">
            {{ role }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import Avatar from 'primevue/avatar'

defineOptions({
  name: 'banner'
})

const props = defineProps({
  quote: {
    type: String,
    required: true
  },
  client: {
    type: String,
    required: true
  },
  role: {
    type: String,
    required: true
  },
  image: {
    type: String,
    required: true
  }
})
</script>
