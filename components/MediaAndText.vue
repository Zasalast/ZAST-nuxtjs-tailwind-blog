<template>
  <div class="media-text">
    <div :class="['media', mediaPosition]">
      <div class="media-content">
        <slot name="content"></slot>
      </div>
      <div v-if="mediaType === 'image'" class="media-image-container">
        <img :src="mediaLink" :alt="mediaAlt" class="media-image" />
      </div>
      <!-- Otros tipos de medios (si es necesario) -->

      <!-- Contenido -->

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
      default: 'https://via.placeholder.com/150',
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
  display: flex;
}

@media (max-width: 1024px) {
  .media-image-container {
    /* Estilos para el contenedor de la imagen */
    width: 30%;
    /* Ajusta según tus necesidades, aquí estamos utilizando el 40% del ancho */
  }
}

@media (max-width: 1024px) {
  .media-image-container {
    /* Estilos para el contenedor de la imagen */
    width: 30%;
    /* Ajusta según tus necesidades, aquí estamos utilizando el 40% del ancho */
  }
}

.media-image {
  /* Estilos para la imagen del medio (puede ajustarse según tus necesidades) */
  max-width: 100%;
  /* Ajustar el ancho máximo de la imagen */
  height: auto;
  /* Permitir que la altura se ajuste proporcionalmente al ancho */
  object-fit: cover;
  /* Asegura que la imagen se ajuste completamente en el contenedor sin distorsiones */
}

.media-content {
  /* Estilos para el contenido del medio (puede ajustarse según tus necesidades) */
  width: 50%;
  /* Ajusta según tus necesidades, aquí estamos utilizando el 60% del ancho */
  padding: 1em;
  /* Ajusta el relleno según tus necesidades */
}

@media (max-width: 1024px) {

  /* Estilos para pantallas más pequeñas, como tabletas */
  .media {
    flex-direction: column;
    /* Apilar elementos en dispositivos más pequeños */
  }

  .media-image-container,
  .media-content {
    width: 90%;
    /* Utilizar el ancho completo en dispositivos más pequeños */
  }
}

@media (min-width: 624px) {

  /* Estilos para pantallas más grandes, como escritorio */
  .media-image-container {
    width: 30%;
    /* Ajusta según tus necesidades, aquí estamos utilizando el 30% del ancho en escritorio */
  }

  .media-content {
    width: 70%;
    /* Ajusta según tus necesidades, aquí estamos utilizando el 70% del ancho en escritorio */
  }
}
</style>
