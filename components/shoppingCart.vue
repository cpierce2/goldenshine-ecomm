<template>
  <!-- creates a stepped form -->
  <v-stepper
    v-model='step'
    :items="steps">
    <!-- template for the first part of the form -->
    <template v-slot:item.1>
      <!-- title -->
      <h3 class="text-h6">Order</h3>
      <!-- table -->
      <v-table>
        <!-- table header -->
        <thead>
          <!-- table row -->
          <tr>
            <!-- row header -->
            <th class='text-center'>Item</th>
            <!-- row header -->
            <th class='px-8'>Image</th>
            <!-- row header -->
            <th>Details</th>
            <!-- row header -->
            <th>Karatage</th>
            <!-- row header -->
            <th>Qty</th>
            <!-- row header -->
            <th>Price</th>
          </tr>
        </thead>

        <!-- table body -->
        <tbody>
          <!-- table body row -->
          <tr v-for='prod in products'>
            <!-- table data -->
            <td>
              <v-checkbox
              :key='id'
              :value='prod'
              v-model='cart'
              />
            </td>
            <!-- table data -->
            <td>
              <!-- table data -->
              <v-list-item :prepend-avatar='prod.image' />
            </td>
            <!-- table data -->
            <td>{{ prod.title }}</td>
            <!-- table data -->
            <td class='text-center'>{{ prod.subTitle }}</td>
            <!-- table data -->
            <td class='text-end'>{{ prod.qty }}</td>
            <!-- table data -->
            <td>{{ '$' + prod.price }}</td>
          </tr>
        </tbody>
      </v-table>
    </template>

    <!-- template for form second section -->
    <template v-slot:item.2>
      <!-- title -->
      <h3 class="text-h6">Shipping</h3>
      <!-- break -->
      <br>

      <!-- radio group for shipping options -->
      <v-radio-group v-model="shipping" label="Delivery Method" aria-required>
        <!-- radio options -->
        <v-radio label="Standard Shipping - $5.99" value="5.99" />
        <v-radio label="Priority Shipping - $10.99" value="10.99" />
        <v-radio label="Express Shipping - $15.99" value="15.99" />
      </v-radio-group>
    </template>

    <!-- template for third section of the form -->
    <template v-slot:item.3>
      <!-- title -->
      <h3 class="text-h6">Confirm</h3>
      <!-- break -->
      <br>

      <!-- sheet to show cart items -->
      <v-sheet :border='true'>
        <!-- creates table -->
        <v-table>
          <!-- table header -->
          <thead>
            <!-- header row -->
            <tr>
              <!-- header -->
              <th class='px-9'>Item</th>
              <!-- header -->
              <th>Details</th>
              <!-- header -->
              <th>Caratage</th>
              <!-- header -->
              <th class="text-end">Qty</th>
              <!-- header -->
              <th class="text-end">Price</th>
            </tr>
          </thead>

          <!-- table body -->
          <tbody>
            <!-- table body row -->
            <tr v-for="(prod, index) in cart" :key="index">
              <!-- table data -->
              <td>
                <!-- table data -->
                <v-list-item :prepend-avatar='prod.image' />
              </td>
              <!-- table data -->
              <td>{{ prod.title }}</td>
              <!-- table data -->
              <td>${{ prod.subTitle }}</td>
              <!-- table data -->
              <td class="text-end"> {{ prod.qty }}</td>
              <!-- table data -->
              <td class="text-end">{{ prod.price }}</td>
            </tr>

            <!-- table row -->
            <tr>
              <!-- table data -->
              <td>Shipping</td>
              <!-- table data -->
              <td></td>
              <!-- table data -->
              <td></td>
              <!-- table data -->
              <td></td>
              <!-- table data -->
              <td class="text-end" v-text=" '$' + shipping"></td>
            </tr>

            <!-- table row -->
            <tr>
              <!-- row header -->
              <th>Total</th>
              <!-- header -->
              <th></th>
              <!-- header -->
              <th></th>
              <!-- header -->
              <th></th>
              <!-- header -->
              <th class="text-end">
                ${{ total }}
              </th>
            </tr>
          </tbody>
        </v-table>
      </v-sheet>
    </template>
  </v-stepper>
</template>

<script>
  // images import 
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

  export default {
    data: () => ({
      shipping: "$" + 0,
      step: 1,
      steps: [
        'Review Item(s)',
        'Select Shipping',
        'Submit',
      ],
      cart: [],
      products: [
        {
          id: 1,
          image: Img1,
          title: 'Layered Necklace',
          subTitle: '18k Gold',
          price: 2634.86,
          qty: 1,
          selected: false,
        },
        {
          id: 2,
          image: Img2,
          title: 'Tube & Chain Mix',
          subTitle: '18k Gold',
          price: 525.64,
          qty: 1,
          selected: false,
        },
        {
          id: 3,
          image: Img3,
          title: 'Choker',
          subTitle: '14k Gold',
          price: 397.44,
          qty: 1,
          selected: false,
        },
        {
          id: 4,
          image: Img4,
          title: 'Earring/Neclace Set w/ Pearls',
          subTitle: '18k Gold',
          price: 210.39,
          qty: 1,
          selected: false,
        },
        {
          id: 5,
          image: Img5,
          title: 'C.D. Bracelet',
          subTitle: '18k Gold',
          price: 195.70,
          qty: 1,
          selected: false,
        },
        {
          id: 6,
          image: Img6,
          title: 'Earring & Snake Chain Set',
          subTitle: '14k Gold',
          price: 156.54,
          qty: 1,
          selected: false,
        },
        {
          id: 7,
          image: Img7,
          title: 'Couple Ring Set',
          subTitle: '14k Gold',
          price: 499.89,
          qty: 1,
          selected: false,
        },
        {
          id: 8,
          image: Img8,
          title: 'Ring w/ Diamonds',
          subTitle: '14k Gold',
          price: 3986.48,
          qty: 1,
          selected: false,
        },
        {
          id: 9,
          image: Img9,
          title: 'Bangle',
          subTitle: '18k Gold',
          price: 335.12,
          qty: 1,
          selected: false,
        },
        {
          id: 10,
          image: Img10,
          title: 'Ethiopian Wedding Ring',
          subTitle: '14k Gold',
          price: 266.25,
          qty: 1,
          selected: false,
        },
        {
          id: 11,
          image: Img11,
          title: 'Sisters Ring Set',
          subTitle: '14k Gold',
          price: 647.46,
          qty: 1,
          selected: false,
        },
        {
          id: 12,
          image: Img12,
          title: 'Wedding Ring Set',
          subTitle: '18k Gold',
          price: 556.49,
          qty: 1,
          selected: false,
        },
      ]
    }),
    methods: {
      // for possible future use
    },
    computed: {
      subtotal() {
          return this.cart.reduce((acc, product) => acc + product.qty * product.price, 0);
      },
      total() {
          return this.subtotal + Number(this.shipping ?? 0);
      },
    },
    components: {
//      ShoppingCart,
    }
  }
</script>