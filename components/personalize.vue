<template>
  <!-- div parent -->
  <div class='landing-cont main-bg'>
    <!-- creates parent grid -->
    <v-row no-gutters>
      <!-- column in the grid -->
      <v-col class='px-16 pt-16' style='background-color: whitesmoke;'>
        <!-- title content for the column -->
        <v-card-title class='text-black' style='line-height: 1; font-size: calc(10pt + 2vw);'>
          Personalization & <br>Engraving
        </v-card-title>

        <!-- item for the column -->
        <v-card-item class='pt-6 pb-16 text-black' style='line-height: 1.2; font-size: calc(12pt + .5vw); padding-left: 1.5vw;'>
          As a thoughtful gift or unique expression of individuality, give your jewelry a 
          special touch with our expert personalization and custom engraving services.
        </v-card-item>

        <!-- creates nested grid -->
        <v-row class='pb-4'>
          <!-- column in nested grid -->
          <v-col>
            <!-- creates appointment button (disabled/no href) -->
            <v-btn
              style='background-color: black;'
            >
              BOOK AN APPOINTMENT
            </v-btn>
          </v-col>
          <!-- creates the second column with the nearest store button -->
          <v-col>
            <!-- creates nearest store button (disabled/no href) -->
            <v-btn
              style='background-color: black;'
            >
              FIND NEAREST STORE
            </v-btn>
          </v-col>
        </v-row>
      </v-col>

      <!-- second column in parent grid -->
      <v-col>
        <!-- column image -->
        <v-img :src='images.img2' class='landing-images'>
          <template v-slot:placeholder>
            <div class="d-flex align-center justify-center fill-height">
              <v-progress-circular
                color="grey-lighten-4"
                indeterminate
              />
            </div>
          </template>
        </v-img>
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
            <v-img :src='images.img5'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- sets disabled shopping link for the image above -->
            <v-dialog>
              <template v-slot:activator="{ props }">
                <!-- sets disabled shopping link for the image above -->
                <v-btn
                  text='Shop Bangels' 
                  class='personalize-links' 
                  v-bind='props'
                  flat
                  @click='dialog = !dialog'
                />
              </template>

              <template v-slot:default="{ isActive }">
                <v-card>
                  <!-- shows future home -->
                  <v-card-item class='text-center my-10'>Future Home of Golden Shine Bangels Collection</v-card-item>
                  <!-- creates a divider -->
                  <v-divider />

                  <!-- creates a divider -->
                  <v-divider />
                  <!-- div parent element -->
                  <div class="pa-4 text-end">
                    <!-- creates the close button -->
                    <v-btn
                      text='Close'
                      class="text-none"
                      color="medium-emphasis"
                      min-width="92"
                      rounded
                      variant="outlined"
                      @click="isActive.value = false"
                    />
                  </div>
                </v-card>
              </template>
            </v-dialog>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img6'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- creates dialog window for Bracelets -->
            <v-dialog>
              <template v-slot:activator="{ props }">
                <!-- sets disabled shopping link for the image above -->
                <v-btn
                  text='Shop Bracelets' 
                  class='personalize-links' 
                  v-bind='props'
                  flat
                  @click='dialog = !dialog'
                />
              </template>

              <template v-slot:default="{ isActive }">
                <v-card>
                  <!-- shows future home -->
                  <v-card-item class='text-center my-10'>Future Home of Golden Shine Bracelets Collection</v-card-item>
                  <!-- creates a divider -->
                  <v-divider />

                  <!-- creates a divider -->
                  <v-divider />
                  <!-- div parent element -->
                  <div class="pa-4 text-end">
                    <!-- creates the close button -->
                    <v-btn
                      text='Close'
                      class="text-none"
                      color="medium-emphasis"
                      min-width="92"
                      rounded
                      variant="outlined"
                      @click="isActive.value = false"
                    />
                  </div>
                </v-card>
              </template>
            </v-dialog>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img7'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- sets disabled shopping link for the image above -->
            <v-dialog>
              <template v-slot:activator="{ props }">
                <!-- sets disabled shopping link for the image above -->
                <v-btn
                  text='Shop Necklaces' 
                  class='personalize-links' 
                  v-bind='props'
                  flat
                  @click='dialog = !dialog'
                />
              </template>

              <template v-slot:default="{ isActive }">
                <v-card>
                  <!-- shows future home -->
                  <v-card-item class='text-center my-10'>Future Home of Golden Shine Necklaces Collection</v-card-item>
                  <!-- creates a divider -->
                  <v-divider />

                  <!-- creates a divider -->
                  <v-divider />
                  <!-- div parent element -->
                  <div class="pa-4 text-end">
                    <!-- creates the close button -->
                    <v-btn
                      text='Close'
                      class="text-none"
                      color="medium-emphasis"
                      min-width="92"
                      rounded
                      variant="outlined"
                      @click="isActive.value = false"
                    />
                  </div>
                </v-card>
              </template>
            </v-dialog>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img8'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- sets disabled shopping link for the image above -->
            <v-dialog>
              <template v-slot:activator="{ props }">
                <!-- sets disabled shopping link for the image above -->
                <v-btn
                  text='Shop Pendants' 
                  class='personalize-links' 
                  v-bind='props'
                  flat
                  @click='dialog = !dialog'
                />
              </template>

              <template v-slot:default="{ isActive }">
                <v-card>
                  <!-- shows future home -->
                  <v-card-item class='text-center my-10'>Future Home of Golden Shine Pendants Collection</v-card-item>
                  <!-- creates a divider -->
                  <v-divider />

                  <!-- creates a divider -->
                  <v-divider />
                  <!-- div parent element -->
                  <div class="pa-4 text-end">
                    <!-- creates the close button -->
                    <v-btn
                      text='Close'
                      class="text-none"
                      color="medium-emphasis"
                      min-width="92"
                      rounded
                      variant="outlined"
                      @click="isActive.value = false"
                    />
                  </div>
                </v-card>
              </template>
            </v-dialog>
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
          <v-img :src='images.img4' class='landing-images'>
            <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
          </v-img>
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
          <v-img :src='images.img3'>
            <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
          </v-img>
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
            <v-img :src='images.img9'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- sets disabled shopping link for the image above -->
            <v-dialog width='350px'>
              <template v-slot:activator="{ props }">
                <!-- sets disabled shopping link for the image above -->
                <v-btn
                  class='personalize-links pt-2' 
                  v-bind='props'
                  variant='plain'
                  @click='dialog = !dialog'
                >In-Store & Vurtual <br> Appointments</v-btn>
              </template>

              <template v-slot:default="{ isActive }">
                <v-card>
                  <v-date-picker show-adjacent-months></v-date-picker>
                  <!-- creates a divider -->
                  <v-divider />

                  <!-- creates a divider -->
                  <v-divider />
                  <!-- div parent element -->
                  <div class="pa-4 text-end">
                    <!-- creates the close button -->
                    <v-btn
                      text='Close'
                      class="text-none"
                      color="medium-emphasis"
                      min-width="92"
                      rounded
                      variant="outlined"
                      @click="isActive.value = false"
                    />
                  </div>
                </v-card>
              </template>
            </v-dialog>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img10'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- sets disabled shopping link for the image above -->
            <v-btn class='personalize-links pt-2' variant='plain'>Full-Service <br> Jeweler</v-btn>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img11'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- sets disabled shopping link for the image above -->
            <v-dialog>
              <template v-slot:activator="{ props }">
                <!-- sets disabled shopping link for the image above -->
                <v-btn
                  text='Payment Options' 
                  class='personalize-links' 
                  v-bind='props'
                  variant='plain'
                  @click='dialog = !dialog'
                />
              </template>

              <template v-slot:default="{ isActive }">
                <v-card>
                  <div class="d-flex justify-space-around py-2">
                    <v-img v-for="payment in payments" :key="payment" :src='payment.img' height='200px' />
                  </div>
                  <!-- creates a divider -->
                  <v-divider />

                  <!-- creates a divider -->
                  <v-divider />
                  <!-- div parent element -->
                  <div class="pa-4 text-end">
                    <!-- creates the close button -->
                    <v-btn
                      text='Close'
                      class="text-none"
                      color="medium-emphasis"
                      min-width="92"
                      rounded
                      variant="outlined"
                      @click="isActive.value = false"
                    />
                  </div>
                </v-card>
              </template>
            </v-dialog>
          </v-col>

          <!-- column in the grid -->
          <v-col>
            <!-- sets image for grid -->
            <v-img :src='images.img12'>
              <template v-slot:placeholder>
                <div class="d-flex align-center justify-center fill-height">
                  <v-progress-circular
                    color="grey-lighten-4"
                    indeterminate
                  />
                </div>
              </template>
            </v-img>
            <!-- sets disabled shopping link for the image above -->
            <v-dialog>
              <template v-slot:activator="{ props }">
                <!-- sets disabled shopping link for the image above -->
                <v-btn 
                  class='personalize-links' 
                  v-bind='props'
                  variant='plain'
                  @click='dialog = !dialog'
                >Ways To Shop</v-btn>
              </template>

              <template v-slot:default="{ isActive }">
                <v-card>
                  <v-list>
                    <v-list-subheader class='text-center'>Ways To Shop</v-list-subheader>

                    <v-list-item
                      v-for="(item, i) in items"
                      :key="i"
                      :value="item"
                      color="primary"
                      variant="tonal"
                    >
                      <template v-slot:prepend>
                        <v-icon :icon="item.icon"></v-icon>
                      </template>

                      <v-list-item-title v-text="item.text"></v-list-item-title>
                    </v-list-item>
                  </v-list>
                  <!-- creates a divider -->
                  <v-divider />

                  <!-- creates a divider -->
                  <v-divider />
                  <!-- div parent element -->
                  <div class="pa-4 text-end">
                    <!-- creates the close button -->
                    <v-btn
                      text='Close'
                      class="text-none"
                      color="medium-emphasis"
                      min-width="92"
                      rounded
                      variant="outlined"
                      @click="isActive.value = false"
                    />
                  </div>
                </v-card>
              </template>
            </v-dialog>
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
  import visa from '@/assets/visa.svg'
  import amex from '@/assets/american-express-card.svg'
  import gPay from '@/assets/google-pay-1.svg'
  import mastercard from '@/assets/mastercard-4.svg'

  import { ref } from 'vue'

  // exports data
  export default {
    data: () => ({
      dialog: ref(true),
      // images array
      images: {
        img1, img2, 
        img3, img4, 
        img5, img6,
        img7, img8,
        img9, img10,
        img11, img12
      },
      payments: [
        {img: visa}, {img: mastercard},
        {img: gPay}, {img: amex}, 
      ],
      items: [
        { text: 'Virtual Appointment', icon: 'mdi-clock' },
        { text: 'In-Person', icon: 'mdi-account' },
        { text: 'Online/Mobile', icon: 'mdi-cellphone-link' },
        { text: 'Call/Text', icon: 'mdi-cellphone-text' },
        { text: 'Chat', icon: 'mdi-chat-processing-outline '}
      ],
    }),
    methods: {
      onClick () {
        this.snackbar = false
      },
    },
    computed: {
      // for possible future use
    },
    components: {
      // 
    }
  }
</script>