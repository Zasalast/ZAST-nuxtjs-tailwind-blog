<!-- media-text.vue -->
<template>
  <div class="media-text">
    <div :class="['media', mediaPosition]">
      <img v-if="mediaType === 'image'" :src="mediaLink" :alt="mediaAlt" class="media-image" />
      <!-- Otros tipos de medios (si es necesario) -->

      <!-- Contenido -->
      <div class="media-content">
        <slot name="content"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    mediaPosition: {
      type: String,
      default: 'default',
    },
    mediaId: {
      type: Number,
      default: 0,
    },
    mediaLink: {
      type: String,
      default: 'https://placeholder.com',
    },
    mediaType: {
      type: String,
      default: 'image',
    },
    mediaAlt: {
      type: String,
      default: 'Media Alt Text',
    },
  },
};
</script>

<style scoped>
/* Estilos adicionales si es necesario */
.media {
  /* Estilos para el contenedor del medio (puede ajustarse según tus necesidades) */
}

.media-image {
  /* Estilos para la imagen del medio (puede ajustarse según tus necesidades) */
}

.media-content {
  /* Estilos para el contenido del medio (puede ajustarse según tus necesidades) */
}
</style>
