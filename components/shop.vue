<template>
  <!-- creates container with the background color -->
  <v-container fluid class='main-bg'>
    <!-- creates a row for the container -->
    <v-row>
      <!-- creates a card -->
      <v-card v-for='prodCard in prodCards'
        :key='prodCard.id'
        elevation='0'
        width='20rem'
        class='mx-16 my-6 main-bg'>
        <!-- loops through the images for the cards -->
        <v-img :src='prodCard.itemImage' height="275px" width='100%' cover/>
        <!-- displays card item through loop iteration -->
        <v-card-title class='text-center' v-text='prodCard.itemName' />
        <!-- provides actions for the cards with a button to drop down for more info -->
        <v-card-actions>
          <!-- creates "see more" expansion panels for the card -->
          <v-expansion-panels>
            <!-- expansion panel template -->
            <v-expansion-panel
              :key='prodCard.id'
              title='Details'
              color='primary'
              elevation='5'
            >
              <!-- text for the expansion panel -->
              <v-expansion-panel-text
                v-text='prodCard.itemDescription' 
                class='text-justify mx-5 my-2' 
              />
              <!-- nested panel text for table content -->
              <v-expansion-panel-text>
                <!-- creates table -->
                <v-table>
                  <!-- table body, no header elements -->
                  <tbody>
                    <!-- first row -->
                    <tr>
                      <!-- displays price title and item price -->
                      <td>{{ prodCard.price }}</td>
                      <td>${{ prodCard.itemPrice }}</td>
                    </tr>
                    <!-- second row -->
                    <tr>
                      <!-- displays wieght title and item weight in ounces -->
                      <td>{{ prodCard.weight }}</td>
                      <td>{{ prodCard.itemWeight }} Ounces</td>
                    </tr>
                    <!-- third row -->
                    <tr>
                      <!-- displays karats title and item karats -->
                      <td>{{ prodCard.karatage }}</td>
                      <td>{{ prodCard.itemKarat }}k</td>
                    </tr>
                  </tbody>
                </v-table>
              </v-expansion-panel-text>
              
              <!-- creates expansion text element for the add to cart button -->
              <v-expansion-panel-text>
                <!-- creates a success "added item to cart" dialog window -->
                <v-dialog>
                  <!-- template for the add to cart button -->
                  <template v-slot:activator="{ props }">
                    <!-- creates the button -->
                    <v-btn 
                      text='Add to Cart'
                      v-bind='props'
                      color='primary'
                      variant='outlined'
                      @click='dialog = !dialog'
                    />
                  </template>

                  <!-- template for the success dialog window -->
                  <template v-slot:default="{ isActive }">
                    <!--  -->
                    <v-fade-transition hide-on-leave>
                      <!-- creates the card that holds the success message -->
                      <v-card
                        class="mx-auto text-center px-6"
                        max-width='500'
                        title="Success">
                        <!-- creates a divider -->
                        <v-divider></v-divider>
                        <!-- div parent -->
                        <div class="py-12 text-center">
                          <!-- shows a circle with checkmark icon -->
                          <v-icon
                            class="mb-6"
                            color="success"
                            icon="mdi-check-circle-outline"
                            size="128" />
                          <!-- displays "item added to cart" text -->
                          <div class="text-h4 font-weight-bold">Item Added to Cart</div>
                        </div>
                        <!-- creates a divider -->
                        <v-divider />
                        <!-- div parent element -->
                        <div class="pa-4 text-end">
                          <!-- creates the close button -->
                          <v-btn
                            class="text-none"
                            color="medium-emphasis"
                            min-width="92"
                            rounded
                            variant="outlined"
                            @click="isActive.value = false"
                          >
                            Close
                          </v-btn>
                        </div>
                      </v-card>
                    </v-fade-transition>
                  </template>
                </v-dialog>
              </v-expansion-panel-text>
            </v-expansion-panel>
          </v-expansion-panels>
        </v-card-actions>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
  // imports images
  import Img1 from '@/assets/gj1.jpg'
  import Img2 from '@/assets/gj2.jpg'
  import Img3 from '@/assets/gj3.jpg'
  import Img4 from '@/assets/gj4.jpg'
  import Img5 from '@/assets/gj5.jpg'
  import Img6 from '@/assets/gj6.png'
  import Img7 from '@/assets/gj7.jpg'
  import Img8 from '@/assets/gj8.png'
  import Img9 from '@/assets/gj9.png'
  import Img10 from '@/assets/gj10.jpg'
  import Img11 from '@/assets/gj11.jpg'
  import Img12 from '@/assets/gj12.jpeg'
  import { ref } from 'vue'

  // creates data for the page to loop through and export
  export default {
    data: () => ({
      show: false,
      dialog: ref(true),
      // data for the loop iteration
      prodCards: [
        {
          itemImage: Img1,
          itemName: 'Layered Necklace',
          itemPrice: 9634.86,
          itemDescription: 'This Necklace has seven layers and embroidered with a beautiful Hibiscus flower pendant resting to the side.',
          itemWeight: 32,
          itemKarat: 22,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img2,
          itemName: 'Tube & Chain Mix',
          itemPrice: 525.64,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 11.3,
          itemKarat: 18,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img3,
          itemName: 'Indian Heritage Choker',
          itemPrice: 397.44,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 10.3,
          itemKarat: 14,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img4,
          itemName: 'Earring & Neclace Pearl Set',
          itemPrice: 210.39,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 9.8,
          itemKarat: 18,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img5,
          itemName: 'Christian Dior Bracelet',
          itemPrice: 195.72,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 4.9,
          itemKarat: 18,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img6,
          itemName: 'Earring and Snake Chain Set',
          itemPrice: 156.54,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 9.4,
          itemKarat: 14,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img7,
          itemName: 'Couple Ring Set',
          itemPrice: 799.89,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 4.2,
          itemKarat: 22,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img8,
          itemName: 'Ring with Diamonds',
          itemPrice: 3986.48,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 2.7,
          itemKarat: 14,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img9,
          itemName: 'Bangle',
          itemPrice: 335.12,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 5.1,
          itemKarat: 18,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img10,
          itemName: 'Ethiopian Wedding Ring',
          itemPrice: 266.25,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 3.2,
          itemKarat: 14,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img11,
          itemName: 'Three Sisters Ring Set',
          itemPrice: 647.46,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 6.7,
          itemKarat: 14,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        },
        {
          itemImage: Img12,
          itemName: 'Wedding Ring Set',
          itemPrice: 556.49,
          itemDescription: 'This is filler content for the sake of taking up space',
          itemWeight: 2.6,
          itemKarat: 18,
          price: 'Price:',
          weight: 'Weight:',
          karatage: 'Karatage:',
        }
      ],
    }),
    created () {
      // empty function for future use
    },
    computed: {
      // empty space for future computed
    },
    methods: {
      // empty space for future methods
    },
    components: {
      // empty space for future components
    },
  }
</script>