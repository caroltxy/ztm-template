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
              grid grid-cols-4
              text-sm
              font-oswald
              text-white
              uppercase
              pt-5
            "
          >
<!--text lg font (font size), text-white (font color), uppercase means change all words into uppercase)-->
            <li>About Us</li>
            <li>Our Menu</li>
            <li>Locations</li>
            <li>Contacts</li>
          </ul>
        </div>
        </div>
      <!--HERO SECTION /NAVIGATION SECTION -->
      <div class="grid grid-cols-2 pb-20 pt-10">
        <!--this is to create 2 columns under hero section-->
        <img
          src="hero-burger.png"
          class="pr-8 mt-10"
          alt=""
        /><!--display burger png on left side of Hero section, mt-10 (margin)-->

        <div>
           <h1
            class="
              text-8xl text-white text-center
              font-lilita
              uppercase
            "
            >
            Class Burger
          </h1>
          <h2
            class="
              text-6xl text-white text-center
              font-lilita
              uppercase
              mt-5
              mb-5
            "
          >
            With Onion
          </h2>
          <p class="text-white font-roboto font-light text-center">
            Our signature burger now comes with onion and cheese. You can customise it to your likings. Freshly made to order, all in a
            Brioche style bun.</p>
        </div>
      </div>
    </div>
    <div id="section-1" class="text-center bg-[url('/about.jpg')] pb-60 bg-cover">
      <h1 class="text-6xl uppercase font-oswald pt-20 px-28">The burger tastes better when you eat it with family</h1>
      <p class="font-roboto font-light text-gray-500 text-lg pt-6 px-24">
        Spend quality time with your family and eat an affordable, nutritious
        and delicious meal together. Not all burgers are fast foods. All our
        burgers are handmade to orders for you and your family members to enjoy.
      </p>
      <div class="text-center">
      <button class="font-oswald uppercase bg-red-500 text-white text-center py-3 px-8">Explore Full Menu</button><!--bg red repsents of background red color-->
      </div>
      </div>
      <div id='section-2'>
        <div class='grid grid-cols-3 text-center pl-20 pr-20 pt-10 pb-10 bg-yellow-500 gap-10'>
        <div>
          <!--refer to www.heroicons.com for star icon - copy the svg and paste into row 80 - 87-->
          <svg xmlns="http://www.w3.org/2000/svg"
          class="h-20 w-20 stroke-1 mx-auto"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
          </svg>
          <h2 class="font-medium font-oswald text-2xl uppercase pt-5 pb-5">Original Recipes</h2>
          <p class="font-light">We use our own secret recipes and only the best ingredients to make our burgers. Starting from patties, sauces, and even buns.</p>
        </div>
        <div>
          <svg xmlns="http://www.w3.org/2000/svg"
        class="h-20 w-20 stroke-1 mx-auto"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="2">
      <path stroke-linecap="round" stroke-linejoin="round" d="M21 15.546c-.523 0-1.046.151-1.5.454a2.704 2.704 0 01-3 0 2.704 2.704 0 00-3 0 2.704 2.704 0 01-3 0 2.704 2.704 0 00-3 0 2.704 2.704 0 01-3 0 2.701 2.701 0 00-1.5-.454M9 6v2m3-2v2m3-2v2M9 3h.01M12 3h.01M15 3h.01M21 21v-7a2 2 0 00-2-2H5a2 2 0 00-2 2v7h18zm-3-9v-2a2 2 0 00-2-2H8a2 2 0 00-2 2v2h12z" />
      </svg>
      <h2 class="font-medium font-oswald text-2xl uppercase pt-5 pb-5">Quality Foods</h2>
      <p class="font-light">We purchase our ingredients from the best suppliers daily, to ensure the freshest quality of our burgers.</p>
      </div>
        <div>
          <svg xmlns="http://www.w3.org/2000/svg"
        class="h-20 w-20 stroke-1 mx-auto"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
        stroke-width="2">
  <path stroke-linecap="round" stroke-linejoin="round" d="M13 10V3L4 14h7v7l9-11h-7z" />
  </svg>
   <h2 class="font-medium font-oswald text-2xl uppercase pt-5 pb-5">Fastest Delivery</h2>
      <p class="font-light">Burgers are best served while it's hot. We delivery to  your door with our speedy delivery partners from the nearest outlet.</p>
  </div>
      </div>
      <div id="section-3">
      <h2 class="text-6xl font-oswald text-red-500 upper font-medium text-center pt-20"> Our Crazy Burgers</h2>
      <p class="text-gray-500 font-light text-xl my-10 px-20 text-center">
      Whether you are looking for the classics, our specialties, or just wraps, salads, and fries. We have it all. We always have something that rewards you tastebud.</p>
      <div class="grid grid-cols-2 px-40 gap-2"> <!--cols 2 = 2 columns gap means the gap width in both pictures-->
          <div id="left-item-column"><!--left item column is merely the variable name - self creation-->
          <div class="border rounded-md border-gray-200 text-left pb-5 mb-5"><!--rounded md - middle-->
          <img src="crispy-chicken.jpg" alt=""/>
          <h3 class="font-oswald font-medium text-2xl uppercase text-gray-500 mt-5 mb-2 ml-5">Christy Chicken</h3>
          <p class="font-light text-gray-500 mb-5 ml-5">Chicken breast, chilli source, tomatoes, pickles, coleslaw</p>
         <span class="bg-amber-800 text-yellow-400 font bold text-xl font-oswald ml-5 rounded rounded-lg px-5 py-2">RM11.99<!--xl make the text size slight bigger-->
          </span>
          </div>
        <Item image="baa-baa.jpg" title="Baa-Baa Black Sheep" description="American Cheese, tomato relish, avocado, juicy lamb patty" price="15.75"/><!--<Item /> is the variable name extracted from Components -> Item.vue from left top page-->
        </div>
            <div id="right-item-column"><!--right item column is merely the variable name - self creation-->
              <div class="border rounded-md border-gray-200 text-left pb-5 mb-5"><!--rounded md - middle-->
               <img src="ultimate-bacon.jpg" alt=""/>
                <h3 class="font-oswald font-medium text-2xl uppercase text-gray-500 mt-5 mb-2 ml-5">Ultimate Bacon</h3>
                <p class="font-light text-gray-500 mb-5 ml-5">House beef patty, cheddar cheese, smokey bacon, onion, mustard</p>
                <span class="bg-amber-800 text-yellow-400 font bold text-xl font-oswald ml-5 rounded rounded-lg px-5 py-2">RM14.99<!--xl make the text size slight bigger-->
                </span><!--SPAN was used within the price object button-->
                 </div>
                 <Item image="double-burger.jpg" title="Double Burger" description="2 beef patties, cheddar cheese, mustard, pickles, tomatoes" price="15.35"/><!--<Item />  is the variable name extracted from Components -> Item.vue from left top page-->
             </div>
              </div>
              <div class= "grid grid-cols-12 font-oswald uppercase text-4xl text-yellow-800 px-40 gap-5"><!--create column gap in between both images = 5-->
                <div class="col-span-5 bg-cover bg-center bg-[url('/fries-bg-1.jpg')] text-right pl-20 pb-10 pt-10"><!--bg cover represents auto resize background picture into the column given-->
                  <h4>Get your <br />
                  free
                  </h4>
                  <h4>Cheese Fries</h4>
                  <button class="uppercase bg-red-500 text-white text-lg py-3 px-8 mt-5">Claim now</button>
                </div>
                <div class="col-span-7 bg-cover bg-center bg-[url('/burger-bg-1.jpg')] text-right pl-10 pr-10 pt-10">
                  <h4>Chrispy <br /><!--br= break the line to separate rows-->
                    Chicken
                    </h4>
                  <h4>Burger <br />
                  is back!
                  </h4>
                  <button class="uppercase bg-red-500 text-white text-lg py-3 px-8 mt-5">Claim now</button>
                </div>
                </div>
                <div class="grid grid-cols-3 px-40 mt-5 gap-5">
                  <img src="offer-1.jpg" alt="" /><img src="offer-2.jpg" alt="" /><img src="offer-3.jpg" alt="" />
                </div>
              </div>
              <div id='section-4' class="px-20 bg-gray-100 py-20">
                <div class='grid grid-cols-2'>
                  <img src="about.png" alt="" class="pl-20" />
                  <h3 class="font-oswald text-5xl uppercase pl-20 pr-4 pt-10 leading-snug">Nothing Brings people Together Like A Good Burger</h3>
                  </div><!--leading-snug : increase paragraph spacing-->
                <p class='text-lg text-gray-500 mt-10'>That's the philosophy that we always believe in. We're a family-owned and operated business, and we're proud to be a part of the community. We do our best to make sure that everyone's happy and having a good time.</p>
                <p class='text-lg text-gray-500 mt-10'>Burgers are what brought us together and what keeps us together. It's something that you can't put a price tag on. More importantly, we are interested in people. It's not just about the food.</p>
              </div>
              <div id="section-5" class='grid grid-cols-5 bg-yellow-500 text-amber-900'>
              <div class="col-span-3 pl-20 pt-16 pb-16">
              <h4 class="font-oswald text-5xl uppercase">Download Mobile App</h4>
              <h4 class="font-oswald text-6xl uppercase">Save up to 20%</h4>
              <p class="text-lg my-7">Bye bye long queues. Order before and your food would be ready in a flash. Enjoy the convenience of ordering food online at any time and from any location.</p><!--my-7 represents margin top & bottom: 7 sizes-->
              <button><img src="/appstore.png" class="h-[50px]" alt="" /></button>
              <button><img src="/googleplay.png" class="h-[50px]" alt="" /></button>
              </div>
              <div class="col-span-2">
                <img src="/eshop.png" class="-mt-10 h-[500px] object-cover" alt="" /><!--mt-10 -> margin top negative 10 (picture go up more than top border, h-[500px] -> pull longer the picture height, object-cover :auto fit the entire pic. image-->
              </div>
               </div>
                  </div>
                   </div>
                      </div>
                        </div>
                          </div>
                            </div>
</template>
