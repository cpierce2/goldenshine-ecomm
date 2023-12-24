<template>
  <!-- creates the toolbar (header), defines height, hides when scrolled on mobile devices, styling and bacground image -->
  <v-toolbar
  height='100'
  class='text-center'
  image='@/assets/dark-gold-hand.jpg'
  scroll-behavior="hide"
  >
  <!-- creates the row for the grid system -->
    <v-row>
      <!-- this is the page header  -->
      <v-col>
        <!-- title -->
        <div class='page-header'>Golden Shine</div>
        <!-- subtitle -->
        <div class='sub-header'>Jewelry Shop</div>
      </v-col>
    </v-row>
  </v-toolbar>
</template>

<script>
  // imports here (if any)

  export default {
    data: () => ({
      // pre-made place for anything page related
      
    }),
    components: {
      // pre-made place for components if any
    }
  }
</script>
