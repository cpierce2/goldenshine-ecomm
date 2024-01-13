<template>
  <div>
    <head>
      <link rel="icon" href="GSJ_icon.ico" type="image/x-icon">
    </head>
  </div>

  <v-app>
    <app-bar />
    <home-view />
    <footer-template />
  </v-app>
  <NuxtPage />
</template>


<script setup>
  // imports styles for the site
  import '@/assets/styles/settings.scss'

  const title = ref('Golden Shine Jewelry')
  const description = ref('Golden Shine Jewelry is an ecommerce site dedicated to selling jewelry to a global market.')

  // This will be reactive when you change title/description above
  useHead({
    title,
    meta: [{
      name: 'description',
      content: description
    }]
  })
</script>
