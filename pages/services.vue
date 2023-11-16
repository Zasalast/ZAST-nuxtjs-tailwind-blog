<template>
  <div class="max-w-screen-xl mx-auto">
    <h2 class="text-3xl font-bold mb-6">Servicios Destacados</h2>

    <div v-for="service in services" :key="service.id" class="mb-8">
      <media-text :media-position="service.mediaPosition || 'default'" :media-id="service.mediaId || 0"
        :media-link="service.mediaLink || 'https://via.placeholder.com/150'" :media-type="service.mediaType || 'image'"
        :media-alt="service.title || 'Media Alt Text'">
        <template v-slot:content>
          <div>
            <p v-if="service.title" class="text-xl font-bold mb-2">{{ service.title }}</p>
            <div class="flex flex-wrap mb-4">
              <span v-for="tech in service.technologies" :key="tech"
                class="mr-2 mb-2 inline-block bg-green-500 text-white px-2 py-1 rounded-full">
                {{ tech }}
              </span>
            </div>
            <p v-if="service.description" class="mb-4 text-gray-700">{{ service.description }}</p>
            <p v-if="service.content" class="mb-4 text-gray-700">{{ service.content }}</p>
          </div>
        </template>
      </media-text>
    </div>
  </div>
</template>

<script>
import servicesData from '../data/services';
import MediaText from "../components/MediaAndText.vue";

export default {
  components: { MediaText },
  data() {
    return {
      services: servicesData,
    };
  },
};
</script>

<style scoped>
/* No se necesitan estilos adicionales aquí, ya que están definidos en media-text.vue */
</style>
