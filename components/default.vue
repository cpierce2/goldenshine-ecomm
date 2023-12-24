<!-- template for the single page application (designed mobile first) -->
<template>
  <!-- displays the app -->
  <v-app full-height>
    <!-- displays the header for the page -->
    <app-bar />
    <!-- displays the tab (main) content for the page -->
    <default-view />
    <!-- displays the footer for the page -->
    <footer />
  </v-app>
</template>

<script setup>
  // imports 
  import AppBar from '@/components/appBar.vue';
  import DefaultView from '@/components/default.vue';
  import footer from '@/components/footer.vue';
</script>
