<template>
  <!-- creates a card to display gold rates api -->
  <v-card>
    <!-- title for the card -->
    <v-card-title>Today's Gold Rate:</v-card-title>
    <!-- creates text element for the card -->
    <v-card-text>
      <!-- fetched api data outputted here -->
      <p>{{ gold.rates }}</p>
    </v-card-text>
  </v-card>
</template>

<script setup>

const { data: gold } = await useFetch('https://api.metalpriceapi.com/v1/latest?api_key=86e012277b37e177afd6b8e282b5fe2c&base=USD&currencies=JPY')

</script>