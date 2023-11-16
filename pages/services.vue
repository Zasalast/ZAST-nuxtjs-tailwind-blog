<template>
  <div class="max-w-screen-xl mx-auto">
    <h2 class="text-3xl font-bold mb-6">Servicios Destacados</h2>

    <div v-for="service in services" :key="service.id" class="mb-8">
      <div class="flex flex-wrap mb-4">
        <span
          v-for="category in service.category"
          :key="category"
          class="mr-2 mb-2 inline-block bg-blue-500 text-white px-2 py-1 rounded-full"
        >
          {{ category }}
        </span>
      </div>

      <media-and-text
        :media-position="service.mediaPosition || 'default'"
        :media-id="service.mediaId || 0"
        :media-link="service.mediaLink || 'https://via.placeholder.com/150'"
        :media-type="service.mediaType || 'image'"
        :media-alt="service.title || 'Media Alt Text'"
      >
        <template v-slot:content>
          <div class="flex flex-col-reverse md:flex-row">
            <div class="md:w-1/2 md:pr-6">
              <p v-if="service.title" class="text-xl font-bold mb-2">{{ service.title }}</p>
              <div class="flex flex-wrap mb-4">
                <span
                  v-for="tech in service.technologies"
                  :key="tech"
                  class="mr-2 mb-2 inline-block bg-green-500 text-white px-2 py-1 rounded-full"
                >
                  {{ tech }}
                </span>
              </div>
              <p v-if="service.description" class="mb-4">{{ service.description }}</p>
              <p v-if="service.content" class="mb-4">{{ service.content }}</p>
            </div>
            <!-- Mostrar la imagen solo si hay un enlace -->
            <img
              v-if="service.mediaLink"
              :src="service.mediaLink"
              :alt="service.title"
              class="w-full h-auto md:w-1/2 object-cover rounded-lg shadow-lg mb-4 md:mb-0"
            />
          </div>
        </template>
      </media-and-text>
    </div>
  </div>
</template>

<script>
import servicesData from '../data/services';

export default {
  data() {
    return {
      services: servicesData,
    };
  },
};
</script>

