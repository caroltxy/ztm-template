<template>
    <div>
        <div class="bg-[url('/menu-page.jpg')] px-20">
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
            <nuxtLink to="/cart">Cart
            ({{$store.getters.totalItems}})
            </nuxtLink><!--hyperlink cart page to cart page-->
          </ul>
        </div>
        </div>
        <h1 class="text-white font-oswald uppercase text-6xl text-center pt-24 pb-28">Our Menu</h1>
        </div>

        <div id="items" class="grid grid-cols-3 mt-10 ml-20 mr-20">
            <MenuItem v-for="burger in items"
            :key="burger.name"
            :item="burger"/>
        </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      items: [],
    };
  },
  mounted() {
    this.$axios.get('items.json').then(
      (response) => {
        this.items = response.data.burgers;
      });
  },
};
</script>
