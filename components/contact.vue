<template>
  <!-- creates container with background color -->
  <v-container fluid class='heigth-fill main-bg'>
    <!-- creates grid -->
    <v-row justify="center">
      <!-- creates the contact form card -->
      <v-card max-width='900'>
        <!-- produces title for the contact form -->
        <v-card-title 
          class='text-center pb-5 pt-6' 
          style='font-size: calc(14pt + 1vw);'>
          Golden Shine Jewlery Contact Form
        </v-card-title>
        <!-- disclaimer -->
        <v-card-text>
          <p class='mx-12 px-12 pb-5'>Thank you for contacting Golden Shine Jelwery. We are thrilled that you are considering 
            our services as your jelwery provider. Please understand that we are working hard to provide 
            the best customer service and quality products online. Which has also led to an increase 
            in contact requests. We typically respond to contact request within three to four business 
            days. We apologize for inconvenience this may cause.
          </p>
          <!-- nested container for the contact form -->
          <v-container>
            <!-- nested grid -->
            <v-row>
              <!-- column for the nested grid -->
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
                <!-- text field for first name -->
                <v-text-field
                  label="Legal first name*"
                  required
                >
                </v-text-field>
              </v-col>
              <!-- column -->
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
                <!-- text field for first name -->
                <v-text-field
                  label="Middle name (optional)"
                  hint="example of helper text only on focus"
                >
                </v-text-field>
              </v-col>
              <!-- column -->
              <v-col
                cols="12"
                sm="6"
                md="4"
              >
                <!-- text field for first name -->
                <v-text-field
                  label="Legal last name*"
                  hint="example of persistent helper text"
                  persistent-hint
                  required
                >
                </v-text-field>
              </v-col>

              <!-- column -->
              <v-col cols="12">
                <!-- text field for email -->
                <v-text-field
                  label="Email*"
                  required
                >
                </v-text-field>
              </v-col>

              <!-- column -->
              <v-col cols="12">
                <!-- creates text field for the comment -->
                <v-text-field
                  prepend-icon='mdi-comment'
                  label="Add message for us*"
                  type="text"
                  required
                >
                </v-text-field>
              </v-col>
              
              <!-- column -->
              <v-col
                cols="12"
                sm="6"
              >
                <!-- selects a user age -->
                <v-select
                  :items="['0-17', '18-29', '30-54', '54+']"
                  label="Age*"
                  required
                >
                </v-select>
              </v-col>
              
              <!-- column -->
              <v-col
                cols="12"
                sm="6"
              >
                <!-- autocomplete action for the iterests -->
                <v-autocomplete
                  :items="['Rings', 'Necklaces',  'Ear Rings', 'Pendants', 'Cuffs', 'Coins', 'Gold Bars', 'Bracelet', 'Anklets', 'Brooch', 'Sizing', 'Engraving', 'Gift Items']"
                  label="Interests*"
                  multiple
                  required
                >
                </v-autocomplete>
              </v-col>
            </v-row>
          </v-container>

          <!--  -->
          <small>*indicates required field</small>
        </v-card-text>
          
        <!-- creates actions for form -->
        <v-card-actions>
          <!-- spacer -->
          <v-spacer />
          <!-- button action -->
          <v-btn
            color="blue-darken-1"
            variant="text"
            @click="dialog = false">
            Close
          </v-btn>
            
          <!-- button action -->
          <v-btn
            color="blue-darken-1"
            variant="text"
            @click="dialog = false">
            Submit
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-row>
  </v-container>
</template>

<script>
  // imports (if any)

  // exports data
  export default {
    data: () => ({
      dialog: false,

    }),
  }
</script>