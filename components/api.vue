<template>
  <!-- creates a card to display gold rates api -->
  <v-card>
    <!-- title for the card -->
    <v-card-title>Today's Gold Rate:</v-card-title>
    <!-- creates text element for the card -->
    <v-card-text>
      <!-- fetched api data outputted here -->
      <pre></pre>
    </v-card-text>
  </v-card>
</template>

<script setup>
  // creates a fetch for api
  fetch('https://api.metalpriceapi.com/v1/latest?api_key=93868a235967cf43d3ceca81c7490453&base=USD&currencies=JPY')
  .then(data => 
  data.json()
  )
  .then(data => {
    console.log(data);
    document.querySelector('pre').innerHTML = JSON.stringify(data.rates);
  })
  .catch(error => console.error(error));
</script>