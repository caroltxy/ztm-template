<template><!-- Note: This is the repetitive/ repeated codings used in the same component!-->
 <div class="border rounded-md border-gray-200 text-left pb-5 mb-5"><!--rounded md - middle, mb-5 = margin botton 5 (give some spaces between 1st & 2nd images)-->
          <img :src="image" alt=""/>
          <h3 class="font-oswald font-medium text-2xl uppercase text-gray-500 mt-5 mb-2 ml-5">{{title}}</h3>
          <p class="font-light text-gray-500 mb-5 ml-5">{{description}}</p>
         <span class="bg-amber-800 text-yellow-400 font bold text-xl font-oswald ml-5 rounded rounded-lg px-5 py-2">RM{{price}}<!--xl make the text size slight bigger-->
          </span>
          </div>
</template>

<script>
export default { props: ['image', 'title', 'description', 'price'] }
</script>
