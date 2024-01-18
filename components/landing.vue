<template>
  <!-- container for the page -->
  <v-container fluid class='landing-cont'>
    <v-container fluid class='landing-vid'>
      <video autoplay loop preload="auto" :src='vids.vid'></video>
    </v-container>
          


    <!-- sheet to show content -->
    <v-sheet
      class="d-flex align-center justify-center flex-wrap text-center mx-auto my-8 px-4 banner banner-bg"
      elevation="0"
      height="250"
      rounded
      max-width="auto"
      width="100%">

      <!-- div parent -->
      <div>
        <!-- title -->
        <h2 class="text-h4 font-weight-black text-purple">Welcome </h2>
        <!-- text -->
        <div class="text-h5 font-weight-medium mb-2">
          You are officially a part of the Golden Shine Jewlery Community!
        </div>
        <!-- sub-text -->
        <p class="text-body-2 mb-4">
          Let us bring you and your loved ones tremendous joy with nothing but the finest Gold jewelry around.
        </p>
      </div>
    </v-sheet>

    <!-- creates grid -->
    <v-row>
      <!-- column -->
      <v-col>
        <!-- container for the grid content -->
        <v-container class='landing-col'>
          <!-- title -->
          <v-card-item>OUR BEGINNING</v-card-item>
          <!-- main title -->
          <v-card-title class='info-title d-flex' style='font-size: calc(14pt + 1vw);'>An Ethical Approach</v-card-title>
          <!-- text content -->
          <v-card-text>
            When we couldn’t find a standard that met ours, we created a new one. We started by 
            creating a rigorous protocol for diamond sourcing that goes beyond current industry 
            practices: Beyond Conflict FreeTM Diamonds which are selected for their ethical and 
            environmentally responsible origins.
            <br><br>
            We were one of the first jewelers to offer blockchain-enabled diamonds at scale, to 
            provide traceability of a diamond’s origin and ownership. Choosing a Brilliant Earth 
            diamond offers unparalleled transparency of your diamond’s provenance.
            <br><br>
            We strive to use 100% recycled precious metals to minimize our footprint and help 
            diminish the negative impacts of metal mining. Precious metals can be recycled 
            repeatedly without degrading their integrity, which means we don’t compromise quality 
            or beauty to make sustainable jewelry.         
          </v-card-text>
        </v-container>
      </v-col>

      <!-- second column for the image -->
      <v-col>
        <!-- shows image -->
        <v-img :src='images.img5' class='landing-images'>
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

    <!-- sheet for more page content -->
    <v-sheet
      class="d-flex align-center justify-center flex-wrap text-center mx-auto px-4 banner"
      elevation="0"
      height="250"
      rounded
      max-width="auto"
      width="100%">

      <!-- div parent -->
      <div>
        <!-- title -->
        <h2 class="text-h4 font-weight-black text-purple">Proposing in 2024?</h2>
        <!-- text content -->
        <div class="text-h5 font-weight-medium mb-2 text-black">
          Take a look at our fine engagment rings on our product page.
        </div>
        <!-- sub title -->
        <p class="text-body-2 mb-4 text-black">
          With a large selection of engagement rings that are sure to WOW her, we are sure you will find the perfect ring for the perfect proposal.
        </p>

        <!-- creates dialog window -->
        <v-dialog>
          <!-- slot for buttons to append to -->
          <template v-slot:activator="{ props }">
            <!-- button for link (disabled no href) -->
            <v-btn 
              v-bind="props" 
              variant="text" 
              color="primary">
              See Proposal Rings
            </v-btn>
          </template>

          <!-- creates template -->
          <template v-slot:default="{ isActive }">
            <!-- creates card -->
            <v-card width='60vw' class='mx-auto text-center' title='Proposal Jewelry'>
              <!-- card text -->
              <v-card-text>
                This area is left blank intentionally
              </v-card-text>

              <!-- creates closing action for the card -->
              <v-card-actions>
                <!-- spacer -->
                <v-spacer />
                <!-- creates an icon button -->
                <v-btn icon='mdi-close' @click='isActive.value = false' />
              </v-card-actions>
            </v-card>
          </template>
        </v-dialog>
      </div>
    </v-sheet>

    <!-- creates grid -->
    <v-row>
      <!-- column in grid -->
      <v-col>
        <!-- image in column -->
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
      </v-col>

      <!-- second column -->
      <v-col>
        <!-- container in column -->
        <v-container class='landing-col'>
          <!-- title -->
          <v-card-item>OUR CRAFTSMANSHIP</v-card-item>
          <!-- main title -->
          <v-card-title class='info-title d-flex' style='font-size: calc(14pt + 1vw);'>Design Sets Us Apart</v-card-title>
          <!-- card content -->
          <v-card-text>
            Our number one goal is to make incomparably beautiful jewelry, just for you. At our 
            San Francisco design studio, our team designs every piece to delight you, from the 
            first time you see it and every day after. We carefully consider the entire piece—the 
            artfully tapered prongs; the hidden accents under the center gem; the precisely curved 
            interior of each band. We obsess over comfort, quality, and durability to ensure that 
            this is jewelry you will cherish for a lifetime.
          </v-card-text>
        </v-container>
      </v-col>
    </v-row>

    <!-- creates card -->
    <v-card
      class="mx-auto text-center landing-col"
      elevation="0"
      max-width="900">
      <!-- image in the card -->
      <v-img 
        :src='images.img6'
        height='auto'
        cover>
        <!-- slot placeholder for the progress -->
        <template v-slot:placeholder>
          <!-- div parent -->
          <div class="d-flex align-center justify-center fill-height">
            <!-- progress indicator -->
            <v-progress-circular
              color="grey-lighten-4"
              indeterminate
            />
          </div>
        </template>
      </v-img>

      <!-- card title -->
      <v-card-title class="wrap text-h4 font-weight-black text-purple">
        'Tis the Season
      </v-card-title>

      <!-- card subtitle -->
      <v-card-subtitle 
        class="wrap text-h5 font-weight-medium d-flex" 
        style='line-height: 1.5;'>
        Find the right gift for that special someone on Santa's Nice List.
      </v-card-subtitle>
      <!-- creates dialog window -->
      <v-dialog>
        <template v-slot:activator="{ props }">
          <!-- button for link -->
          <v-btn 
            v-bind="props" 
            variant="text" 
            color="primary">
            See Seasonal Jelwery
          </v-btn>
        </template>

        <!-- template -->
        <template v-slot:default="{ isActive }">
          <!-- creates card -->
          <v-card width='60vw' class='mx-auto text-center' title='Seasonal Jewelry'>
            <!-- card text -->
            <v-card-text>
              This area is left blank intentionally
            </v-card-text>

            <!-- creates card actions -->
            <v-card-actions>
              <!-- spacer -->
              <v-spacer />
              <!-- button to close dialog -->
              <v-btn icon='mdi-close' @click='isActive.value = false' />
            </v-card-actions>
          </v-card>
        </template>
      </v-dialog>
    </v-card>

    <!-- creates a image carousel -->
    <v-carousel 
      cycle 
      hide-delimiters 
      show-arrows='hover'
      class='my-6'>
      <!-- dynamically adds images -->
      <v-carousel-item v-for='item in carouselItems' :key='item' :src='item.img'>
        <template v-slot:placeholder>
          <div class="d-flex align-center justify-center fill-height">
            <v-progress-circular
              color="grey-lighten-4"
              indeterminate
            ></v-progress-circular>
          </div>
        </template>
      </v-carousel-item>
    </v-carousel>
  </v-container>
</template>

<script>
  // imports
  import vid from '@/assets/made_to_shine.mp4'
  import img1 from '@/assets/Ankle_Bracelet.jpg'
  import img2 from '@/assets/midas-hp-slider3.jpg'
  import img3 from '@/assets/mens2.png'
  import img4 from '@/assets/hero-hd.jpg'
  import img5 from '@/assets/proposal2.jpeg'
  import img6 from '@/assets/christmas_jewelry.jpg'
  import img7 from '@/assets/luxury-black-silk.jpg'

  // exports data
  export default {
    data: () => ({
      vids: {
        vid
      },
      images: {
        img4, img5, img6, img7
      },
      carouselItems: [
        {img: img1},
        {img: img2},
        {img: img3}
      ],
    }),
    components: {
      // pre-made for additional components if needed
    }
  }
</script>