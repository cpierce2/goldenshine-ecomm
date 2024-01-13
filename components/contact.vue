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
          style='font-size: calc(10pt + 1vw);'>
          Golden Shine Jewlery Contact Form
        </v-card-title>
        <!-- disclaimer -->
        <v-card-text>
          <p class='mx-4 pb-4 text-justify'>
            Thank you for contacting Golden Shine Jelwery. We are thrilled that you are considering 
            our services as your jelwery provider. Please understand that we are working hard to provide 
            the best customer service and quality products online. Which has also led to an increase 
            in contact requests. We typically respond to contact request within three to four business 
            days. We apologize for inconvenience this may cause.
          </p>
          <!-- nested container for the contact form -->
          <v-form ref='form'>
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
                  label="First name*"
                  hint='"John"'
                  :rules='firstNameRules'
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
                  label="Last name*"
                  hint='"Doe"'
                  :rules='lastNameRules'
                  required
                >
                </v-text-field>
              </v-col>

              <!-- column -->
              <v-col cols="12">
                <!-- text field for email -->
                <v-text-field
                  label="Email*"
                  hint='john_doe@email.com'
                  :rules='emailRules'
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
                  :rules='messageRules'
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
                  :items="ages"
                  label="Age*"
                  :rules="ageRules"
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
                  :items="items"
                  label="Interests*"
                  :rules="interestRules"
                  multiple
                  required
                >
                </v-autocomplete>
              </v-col>
            </v-row>
          </v-form>

          <!--  -->
          <small>*indicates required field</small>
        </v-card-text>
          
        <!-- creates actions for form -->
        <v-card-actions>
          <!-- spacer -->
          <v-spacer />
          <!-- button action -->
          <v-btn
            text='Reset'
            color="blue-darken-1"
            variant="text"
            @click="reset" 
          />
          
          <v-dialog>
            <!-- template for the add to cart button -->
            <template v-slot:activator="{ props }">
              <!-- creates the button -->
              <v-btn 
                text='Submit'
                v-bind='props'
                v-model='cartItems'
                color='blue-darken-1'
                variant='text'
                @click='dialog = !dialog'
              />
            </template>

            <!-- template for the success dialog window -->
            <template v-slot:default="{ isActive }">
              <v-card
                class="mx-auto text-center px-6"
                max-width='500'
                title='Thank You'>
                <!-- creates a divider -->
                <v-divider />
                <!-- div parent -->
                <div class="py-12 text-center">
                  <!-- shows a circle with checkmark icon -->
                  <v-icon
                    class="mb-6"
                    color="success"
                    icon="mdi-check-circle-outline"
                    size="128" 
                  />
                  <!-- displays "item added to cart" text -->
                  <div class="text-h4 font-weight-bold">Form Submitted</div>
                  <v-divider />
                  <div class='pt-3 my-auto'>We have recieved your contact form and will reach out within 3-5 business days.</div>
                </div>
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
      name: '',
      firstNameRules: [
        v => !!v || 'First name is required',
        v => (v && v.length <= 18) || 'Name must be less than 18 characters'
      ],
      lastNameRules: [
        v => !!v || 'Last name is required'
      ],
      emailRules: [
        v => !!v || 'Email is required'
      ],
      messageRules: [
        v => !!v || 'Message is required'
      ],
      ageRules: [
        v => !!v || 'Age is required'
      ],
      interestRules: [
        v => !!v || 'Interest is required'
      ],
      select: null,
      items: [
        'Rings', 'Necklaces', 'Ear Rings', 
        'Pendants', 'Cuffs', 'Coins', 
        'Gold Bars', 'Bracelet', 'Anklets', 
        'Brooch', 'Sizing', 'Engraving', 
        'Gift Items'
      ],
      ages: [
        '0-17', 
        '18-29', 
        '30-54', 
        '54+'
      ],
      checkbox: false,
    }),
    methods: {
      async validate () {
        const { valid } = await this.$refs.form.validate()

        if (valid) alert('Form is valid')
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
    },
  }
</script>