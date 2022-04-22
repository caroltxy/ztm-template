<template>
    <div>
    <div id="header" class="bg-[url('/hero-bg.jpg')] pl-20 pr-20">
      <!--pl: move the hero jpg to margin padding left, pr: move to margin pading right)-->
      <div id="menu" class="grid grid-cols-2 pt-5 pb-5">
        <!--pt: move to top padding margin 5; pb-padding bottom margin to 5-->
        <div id="menu-left">
          <img src="logo.png" class="w-[150px]" alt="" />
        </div>
        <div id="menu-right">
          <ul
            class="
              grid grid-cols-5
              text-sm
              font-oswald
              text-white
              uppercase
              pt-5
            "
          >
<!--text lg font (font size), text-white (font color), uppercase means change all words into uppercase)-->
            <li>About Us</li>
            <NuxtLink to ="/menu">Our Menu</NuxtLink><!--hyperlink cart page to our menu page-->
            <li>Locations</li>
            <li>Contacts</li>
            <nuxtLink to="/cart">Cart</nuxtLink><!--hyperlink cart page to cart page-->
          </ul>
        </div>
    </div>
    <h1 class="text-white font-oswald uppercase text-6xl text-center pt-16 pb-28">
            Shopping Cart
        </h1>
    </div>
    <table class="table-auto w-2/3 mt-20 mx-auto mb-20">
      <thead>
          <tr><!--table rows-->
              <th class="text-left">Name</th><!--table header-->
              <th class="text-center">Price</th><!--table header-->
              <th>Quantity</th><!--table header-->
              <th class="text-center">Total</th><!--table header-->
              <th>Remove</th><!--table header-->
            </tr>
      </thead>
      <tbody><!--body of the table-->
          <tr v-for="order in $store.state.orders" :key="order.name" class="font-oswald uppercase text-2xl border-b"><!--tr represents table rows-->
              <td class="py-10">{{ order.name }}</td>
              <td class="text-right">RM {{ order.price.toFixed(2) }}</td>
              <td class="text-center">{{ order.quantity }}</td>
              <td class="text-right">RM {{(order.price*order.quantity).toFixed(2) }}</td>
             <td class="text-center"><button @click="removeItem(order.name)">❌</button></td> <!--go to website called https://emojipedia.org/ then copy X emoji and paste over here-->
           </tr>
          </tbody>
          <tfoot>
            <tr class="font-oswald font-bold text-2xl bg-gray-100 uppercase">
              <td class="py-10" colspan="3">Total</td><!--colspan 3 = move the grand total figures to 3rd column under column header "total"-->
              <td class="text-right">RM {{ total.toFixed(2) }}</td>
            </tr>
          <tr>
            <td colspan="3">
              <input id="email" type="email" placeholder="Please email your email" class="w-full border border-gray-300 text-xl mt-5 py-3 px-2" /><!--text xl - enlarge xl size, w-full means to draw an email box in full entire of 3 columns-->
            </td>
            <td colspan="2" class="text-right">
              <button class="font-oswald uppercase bg-red-500 text-white text-xl py-3 px-2 ml-5 mt-5" @click="submitorder">
                Confirm My Order
              </button>
            </td>
          </tr>
          </tfoot>
        </table>
    </div>
</template>
<script>
export default {
  computed: {
    total() {
      let total = 0;
      this.$store.state.orders.forEach((order) => {
        total = total + order.price * order.quantity;
      });
      return total;
    },
  },
  methods: {
    removeItem(name) {
      this.$store.commit('removeItem', name);
    },
    submitOrder() {
      this.$axios.post('/.netlify/functions/email', { email: document.getElementById('email').value, orders: this.$store.state.orders, });
    },
  },
};
</script>
