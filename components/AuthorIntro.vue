<template>
  <div class="mb-6">
    <h2
      class="mt-6 text-4xl text-gray-700 font-bold capitalize dark:text-blue-200"
    >
      👋 Hola ,   Buen día!

    </h2>
    <p class="mt-8 mb-4 dark:bg-gray-800 dark:text-blue-200 text-justify">
      {{ siteMetadata.description }}
    </p>
  </div>
</template>

<script>

import siteMetaInfo from "@/data/sitemetainfo";
export default {

  data: () => {
    return {
      siteMetadata: siteMetaInfo,
    };
  },
};
</script>
