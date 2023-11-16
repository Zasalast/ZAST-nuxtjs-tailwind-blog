<template>
  <div>
    <h2>Servicios Destacados</h2>
    <p></p>

    <div v-for="category in uniqueCategories" :key="category">
      <h3>{{ category }}</h3>
      <div v-for="service in servicesByCategory(category)" :key="service.id">
        <media-text
          :media-position="service.mediaPosition"
          :media-id="service.mediaId"
          :media-link="service.mediaLink"
          :media-type="service.mediaType"
        >
          <template v-slot:content>
            <p><strong>{{ service.title }}</strong></p>
            <p>{{ service.description }}</p>
            <!-- Mostrar la imagen -->
            <img :src="service.mediaLink" :alt="service.title" class="service-image" />
          </template>
        </media-text>
      </div>
    </div>
  </div>
</template>

<script>
import servicesData from '../data/services';

export default {
  data() {
    return {
      servicesData: servicesData,
    };
  },
  computed: {
    uniqueCategories() {
      const technologies = this.servicesData.reduce((acc, service) => acc.concat(service.technologies), []);
      return [...new Set(technologies)];
    },
  },
  methods: {
    servicesByCategory(category) {
      return this.servicesData.filter(service => service.technologies.includes(category));
    },
  },
};
</script>

<style scoped>
/* Estilo adicional si es necesario */
.service-image {
  max-width: 100%; /* Ajustar el ancho máximo de la imagen */
  height: auto; /* Permitir que la altura se ajuste proporcionalmente al ancho */
}
</style>
