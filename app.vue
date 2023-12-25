<template>
  <div>
    <head>
      <meta property="og:url" content="https://www.your-domain.com/your-page.html" />
      <meta property="og:type" content="website" />
      <meta property="og:title" content="Your Website Title" />
      <meta property="og:description" content="Your description" />
      <meta property="og:image" content="https://www.your-domain.com/path/image.jpg" />
    </head>
  </div>

  <v-app>
    <app-bar />
    <home-view />
    <footer-template />
  </v-app>
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
