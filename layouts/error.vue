<template>
  <div class="flex items-center justify-center h-screen">
    <svg class="absolute h-screen w-screen" width="776px" height="550px" viewBox="0 0 776 550" version="1.1" xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink">
      <!-- Generator: Sketch 49 (51002) - http://www.bohemiancoding.com/sketch -->
      <desc>Created with Sketch.</desc>
      <defs></defs>
      <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
        <g id="404-Error">
          <g id="background" transform="translate(-84.000000, -124.000000)">
            <rect id="Rectangle" fill="#FFAD26" transform="translate(452.820508, 147.004464) rotate(35.000000) translate(-452.820508, -147.004464) "
              x="432.820508" y="50.0044642" width="40" height="194" rx="20"></rect>
            <rect id="Rectangle" fill="#FAA053" transform="translate(861.972075, 89.495336) rotate(35.000000) translate(-861.972075, -89.495336) "
              x="844.472075" y="-7.50466407" width="35" height="194" rx="17.5"></rect>
            <rect id="Rectangle" fill="#FF6767" transform="translate(721.924195, 662.061395) rotate(35.000000) translate(-721.924195, -662.061395) "
              x="706.924195" y="617.061395" width="30" height="90" rx="15"></rect>
            <rect id="Rectangle" fill="#FABB53" transform="translate(68.417046, 381.746729) rotate(35.000000) translate(-68.417046, -381.746729) "
              x="58.4170463" y="276.746729" width="20" height="210" rx="10"></rect>
            <rect id="Rectangle" fill="#FABB53" transform="translate(418.160254, 94.004464) rotate(35.000000) translate(-418.160254, -94.004464) "
              x="408.160254" y="-2.99553583" width="20" height="194" rx="10"></rect>
          </g>
        </g>
      </g>
    </svg>
    <div class="relative flex justify-around">
      <div class="text-100xl font-bold mx-10 flex items-center">
        404
      </div>
      <div class="mx-10">
        <p class="text-xl font-xl mb--8">There’s nothing here!</p>
        <p class="my-10">Not all who wander are lost. But you certainly are</p>
        <nuxt-link :to="{ name: 'posts' }" class="no-underline px-6 py-4 border border-grey rounded-full bg-grey-light text-black uppercase text-sm font-bold hover:bg-white">Go To Posts</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>
  export default {

  }

</script>
