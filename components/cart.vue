<template>
  <!-- displays shopping cart vue file -->
  <ShoppingCart /> 
</template>

<script>
  // imports
  import ShoppingCart from '@/components/shoppingCart.vue'

  // exports data
  export default {
    data: () => ({
      cart: null,
    }),

    computed: {
      // for possible future use
    },

    methods: {
      // for possible future use
    },
    // components for cart.vue
    components: {
      ShoppingCart,
    }
  }
</script>