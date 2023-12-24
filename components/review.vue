<template>
  <!-- div parent with background color -->
  <div class='main-bg'>
    <!-- creates the rate purchase card -->
    <v-card
      class="mx-auto"
      color="purple"
      elevation="10"
      width="360"
    >
      <!-- nested div parent -->
      <div class="d-flex justify-between">
        <!-- card title -->
        <v-card-title class="flex-grow-1 flex-column align-start">
          <!-- text content -->
          <div class="text-h5">
            Charm Bracelete
          </div>
          <!-- text content -->
          <div class="text-h6 font-weight-thin">Seasonal Jewelry</div>
          <!-- text content -->
          <div class="text-h6 font-weight-thin">(22k)</div>
        </v-card-title>
        <!-- image in the card -->
        <v-img
          contain
          height="125px"
          :src="images.img1"
          style="flex-basis: 125px"
          class="flex-grow-0"
        ></v-img>
      </div>
      <!-- divider -->
      <v-divider></v-divider>
      <!-- creates rating action -->
      <v-card-actions class="pa-4">
        Rate your purchase
        <!-- spacer -->
        <v-spacer></v-spacer>
        <!-- shows the rating bar -->
        <span class="text-grey-lighten-2 text-caption me-2">
          ({{ rating }})
        </span>
        <!-- rating -->
        <v-rating
          v-model="rating"
          color="white"
          active-color="yellow-accent-4"
          half-increments
          hover
          size="18"
        ></v-rating>
      </v-card-actions>
    </v-card>

    <!-- creates review card -->
    <v-card
      class="d-flex flex-column mx-auto py-8 mt-6"
      elevation="10"
      height="500"
      width="360"
    >
      <!-- div for title -->
      <div class="d-flex justify-center mt-auto text-h5 ">
        Golden Shine Reviews
      </div>
      <!-- div parent -->
      <div class="d-flex align-center flex-column my-auto">
        <!-- 4.8/5 text -->
        <div class="text-h2 mt-5">
          4.8
          <span class="text-h6 ml-n3">/5</span>
        </div>

        <!-- shows rating -->
        <v-rating
          :model-value="4.8"
          color="yellow-darken-3"
          half-increments
        ></v-rating>
        <!-- identifies how many ratings -->
        <div class="px-3">3,360 ratings</div>
      </div>
      <!-- creates a 1-5 star list -->
      <v-list
        bg-color="transparent"
        class="d-flex flex-column-reverse"
        density="compact"
      >
        <!-- creates the list item -->
        <v-list-item v-for="(rating,i) in 5" :key="i">
          <!-- shows rating progression by star -->
          <v-progress-linear
            :model-value="rating * 15"
            class="mx-n5"
            color="yellow-darken-3"
            height="20"
            rounded
          ></v-progress-linear>
          <!-- creates a slot to prepend the rating -->
          <template v-slot:prepend>
            <!-- displays star rating icon -->
            <span>{{ rating }}</span>
            <!-- rating star icon -->
            <v-icon icon="mdi-star" class="mx-3"></v-icon>
          </template>
          <!-- slot for # of ratings -->
          <template v-slot:append>
            <!-- div parent -->
            <div class="rating-values">
              <!-- multiplies rating by 1 star -->
              <span class="d-flex justify-end"> {{ rating * 224 }} </span>
            </div>
          </template>
        </v-list-item>
      </v-list>
    </v-card>

    <!-- creates reviw quote card from twitter (X) -->
    <v-card
      class="mx-auto mt-6"
      color="primary"
      theme="dark"
      max-width="400"
      :prepend-icon='icons.Xicon'
      title="Twitter"
    >
      <!-- quote -->
      <v-card-text class="text-h5 py-2">
        "Thank you GSJ, my now WIFE absolutely LOVED 😍 the ring I got from y'all"
      </v-card-text>
      <!-- creates actions for the quoted card -->
      <v-card-actions>
        <!-- list item -->
        <v-list-item class="w-100">
          <!-- slot template -->
          <template v-slot:prepend>
            <!-- avatar -->
            <v-avatar
              color="grey-darken-3"
              image="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"
            ></v-avatar>
          </template>
          <!-- shows user name -->
          <v-list-item-title>John Smith</v-list-item-title>
          <!-- shows verified customer -->
          <v-list-item-subtitle>Verified GSJ Customer</v-list-item-subtitle>
          <!-- slot prepend -->
          <template v-slot:append>
            <!-- div parent -->
            <div class="justify-self-end">
              <!-- heart icon -->
              <v-icon class="me-1" icon="mdi-heart" />
              <!-- shows how many hearts -->
              <span class="subheading me-2">256</span>
              <!-- creates a dot space -->
              <span class="me-1">·</span>
              <!-- share variant icon -->
              <v-icon class="me-1" icon="mdi-share-variant"></v-icon>
              <!-- shows how many shares -->
              <span class="subheading">45</span>
            </div>
          </template>
        </v-list-item>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
  // imports
  import Xicon from '@/assets/icons/Xicon.vue';
  import img1 from '@/assets/gj14.webp'

  //exports for the page
  export default {
    data: () => ({
      show: false,
      icons: {
        Xicon,
      },
      images: {
        img1
      }
    }),
    components: {
      // for future use if applicable
    }
  }
</script>