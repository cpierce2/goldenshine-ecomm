<template>
  <!-- creates a card to display gold rates api -->
  <v-card>
    <!-- title for the card -->
    <v-card-title>Today's Gold Rate:</v-card-title>
    <!-- creates text element for the card -->
    <v-card-text>
      <!-- fetched api data outputted here -->
      <div id='display'></div>
    </v-card-text>
  </v-card>
</template>

<script setup>

  //const { data: gold } = await useFetch('https://api.metalpriceapi.com/v1/latest?api_key=86e012277b37e177afd6b8e282b5fe2c&base=USD&currencies=JPY')

  const apiEndpoint = ("https://jsonplaceholder.org/posts");

  const getData = async () => {
    const res = await fetch(apiEndpoint);
    const data = await res.json();
    return data
  }

  const displayUsers = async () => {
    const payload = await getData();

    let dataDisplay = payload.map((object) => {
    const { slug } = object;

    return `
      <div>
        <p>${slug}</p>
      </div>
    `
  })
    console.log(dataDisplay)
    document.getElementById('display').innerHTML = dataDisplay[0];
  }

  displayUsers();
</script>