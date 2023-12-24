<template>
  <!-- div parent -->
  <div class='landing-cont main-bg'>
    <!-- creates parent grid -->
    <v-row no-gutters>
      <!-- column in the grid -->
      <v-col class='px-16 pt-16' style='background-color: whitesmoke;'>
        <!-- title content for the column -->
        <v-card-title class='text-black' style='line-height: 1; font-size: calc(18pt + 2vw); padding-left: 1.5vw;'>
          Personalization & <br>Engraving
        </v-card-title>

        <!-- item for the column -->
        <v-card-item class='pt-6 pb-16 text-black' style='line-height: 1.2; font-size: calc(12pt + .5vw); padding-left: 1.5vw;'>
          As a thoughtful gift or unique expression of individuality, give your jewelry a 
          special touch with our expert personalization and custom engraving services.
        </v-card-item>

        <!-- item for the buttons -->
        <v-card-item>
          <!-- creates nested grid -->
          <v-row>
            <!-- column in nested grid -->
            <v-col>
              <!-- creates appointment button (disabled/no href) -->
              <v-btn
                class='text-h6 pa-2 ma-2'
                style='background-color: black;'
              >
                BOOK AN APPOINTMENT
              </v-btn>
            </v-col>
            <!-- creates the second column with the nearest store button -->
            <v-col>
              <!-- creates nearest store button (disabled/no href) -->
              <v-btn
                class='text-h6 pa-2 ma-2'
                style='background-color: black;'
              >
                FIND NEAREST STORE
              </v-btn>
            </v-col>
          </v-row>
        </v-card-item>
      </v-col>

      <!-- second column in parent grid -->
      <v-col>
        <!-- column image -->
        <v-img :src='images.img2' class='landing-images' />
      </v-col>
    </v-row>

    <!-- creates sheet element for the page -->
    <v-sheet
      class="d-flex align-center justify-center flex-wrap text-center mx-auto my-8 px-4 banner"
      elevation="0"
      rounded
      max-width="auto"
      width="100%"
    >
      <!-- div parent container -->
      <div>
        <!-- h2 title -->
        <h2 class="text-h4 font-weight-black text-purple">Jewelry For Any Occasion</h2>

        <!-- content in parent div -->
        <div class="text-h5 font-weight-medium mb-2 personalize-links" >
          Checkout our seasonal and everyday jewelry guarunteed to smile brighter than the jewelry itself. 
        </div>

        <!-- creates grid with links set to dissapear on smaller screens -->
        <v-row>
          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img5' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links' flat>Shop Bangels</v-btn>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img6' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links' flat>Shop Bracelets</v-btn>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img7' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links' flat>Shop Necklaces</v-btn>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img8' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links' flat>Shop Pendants</v-btn>
          </v-col>
        </v-row>
      </div>
    </v-sheet>

    <!-- creates grid -->
    <v-row no-gutters class='mt-6'>
      <!-- column in grid -->
      <v-col>
        <!-- created div parent div -->
        <div class='text-center text-black'>
          <!-- image for the div -->
          <v-img :src='images.img4' class='landing-images' />
          <!-- title for the parent -->
          <v-card-title>Custom Engraving</v-card-title>
          <!-- content for the parent div -->
          <v-card-item>Create a one-of-a-kind treasure with handwritten messages, meaningful 
            dates, names, or special symbols. With our state-of-the-art machinery, the 
            possibilities are endless.
          </v-card-item>
        </div>
      </v-col>

      <!-- second column of grid -->
      <v-col>
        <!-- parent div -->
        <div class='text-center text-black'>
          <!-- image for the parent div -->
          <v-img :src='images.img3' />
          <!-- title for the parent div -->
          <v-card-title>Done In A Day*</v-card-title>
          <!-- content for the parent div -->
          <v-card-item >We’re proud to offer same-day, in-store engraving services. Visit your 
            local Jared store to meet with a jewelry expert and discover the possibilities.
          </v-card-item>
        </div>
      </v-col>
    </v-row>

    <!-- creates sheet element for the page -->
    <v-sheet
      class="d-flex align-center justify-center flex-wrap text-center mx-auto my-8 px-4 banner"
      elevation="0"
      rounded
      max-width="auto"
      width="100%"
    >
      <!-- div parent container -->
      <div>
        <!-- h2 title -->
        <h2 class="text-h4 font-weight-black text-purple">Shop Personalized & Engravable Jewelry Online</h2>

        <!-- content in parent div -->
        <div class="text-h5 font-weight-medium mb-2 personalize-links" >
          Can’t make it to a store? Create one-of-a-kind jewelry with our online personalization services. 
        </div>

        <!-- creates grid with links set to dissapear on smaller screens -->
        <v-row>
          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img9' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links pt-2' variant='plain'>In-store & Virtual <br> Appointments</v-btn>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img10' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links pt-2' variant='plain'>Full-Service <br> Jeweler</v-btn>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img11' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links' variant='plain'>Payment Options</v-btn>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img12' />
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links' variant='plain'>Ways to Shop</v-btn>
          </v-col>
        </v-row>
      </div>
    </v-sheet>
  </div>
</template>

<script>
  // imports
  import img1 from '@/assets/Lookbook.webp'
  import img2 from '@/assets/Personalization_Header.jpg'
  import img3 from '@/assets/engraving1.jpg'
  import img4 from '@/assets/engraving2.jpg'
  import img5 from '@/assets/gj14.jpg'
  import img6 from '@/assets/gj15.webp'
  import img7 from '@/assets/gj16.webp'
  import img8 from '@/assets/gj25.jpg'
  import img9 from '@/assets/Virtual_Appointments.webp'
  import img10 from '@/assets/FullService_Jeweler.webp'
  import img11 from '@/assets/Payment_Options.webp'
  import img12 from '@/assets/Ways_to_Shop.webp'

  // exports data
  export default {
    data: () => ({
      // images array
      images: {
        img1, img2, 
        img3, img4, 
        img5, img6,
        img7, img8,
        img9, img10,
        img11, img12
      }
    }),
    methods: {
      // for possible future use
    },
    computed: {
      // for possible future use
    },
    components: {
      // for possible future use    
    }
  }
</script>