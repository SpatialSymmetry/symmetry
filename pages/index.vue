

<template>
  <div class="w-full min-h-screen bg-gray-950">

    <section class="max-w-screen-sm mx-auto p-4 pt-12">
      <h1 class="text-gray-200 font-extrabold md:font-extrabold text-xl md:text-2xl tracking-tighter">Symmetry Engineering Firm.</h1>
      <p class="mt-4 mx-6 text-gray-400 text-sm md:text-base">Active in an array of engineering fields including computer software and hardware, electrical and mechanical systems, with an strong emphasis on scientific method. To contact us, fill the <a href="#target" class="border-b-2 border-white text-gray-300">form</a> and we'll be in touch.</p>
    </section>
    
    <section class="max-w-screen-sm flex flex-col mx-auto p-8 pt-8 ">
      <div class="grid grid-cols-3 grid-rows-3 gap-2 md:gap-3">
        <div class="h-16 md:h-32 bg-gray-400 rounded-lg"></div>
        <div class="bg-gray-400 row-span-2 rounded-lg"></div>
        <div class="bg-gray-400 rounded-lg"></div>
        <div class="bg-gray-400 row-span-2 rounded-lg"></div>
        <div class="bg-gray-400 row-span-2 rounded-lg"></div>
        <div class="bg-gray-400 rounded-lg"></div>
      </div>
      <p class="text-gray-500 pt-3 text-xs md:text-sm"># Interdependent harmonic oscillation. An abstract phenomenon commonly observed in many distinct areas of nature in many different forms, as if by design.</p>
    </section>


    <section class="max-w-screen-sm flex flex-col mx-auto p-8 pt-8 ">
      <p class="text-gray-200 font-bold">Published Articles</p>
      <div class="bg-gray-300 text-xs md:text-sm text-gray-900 m-2 p-2 border rounded">
        No articles published yet.
      </div>
    </section>

    <section class="max-w-screen-sm mx-auto flex flex-col gap-2 p-8 pt-4 pb-32" id="target">
      <p class="text-gray-200 font-bold">Proposition Form</p>
      <p class="text-gray-500 px-3 py-1 text-xs md:text-sm">
      We select projects not solely for their financial return, but for their alignment with our intellectual interests. We primarily focus on solving simple problems—or a collection of simple problems—using a strictly first-principles and modular approach, aiming for solutions that will remain effective for decades to come. Currently, our focus is more on software.</p>

      <textarea rows="1" placeholder="Please introduce yourself." class="bg-gray-300 rounded mx-2 p-2 text-sm"></textarea>
      <textarea rows="1" placeholder="Tell us about the problem you're trying to solve." class="bg-gray-300 rounded mx-2 p-2 text-sm"></textarea>
      <textarea rows="1" placeholder="How could we contact you?" class="bg-gray-300 rounded mx-2 p-2 text-sm"></textarea>
      <p class="text-gray-500 px-3 py-1 text-xs md:text-sm"> # Please explain in length. You can expand input fields by dragging down from bottom-right corner.
      </p>

      <button type="submit" class="bg-blue-500 w-fit text-xs md:text-sm hover:bg-blue-600 text-white font-bold mx-3 py-2 px-4 rounded">Submit</button>
    </section>

  </div>
</template>


<style scoped>
/* Keyframes for scaling animation */
@keyframes scalePulse {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
}

/* Keyframes for subtle move */
@keyframes subtleMove {
  0%, 100% {
    transform: translate(0, 0);
  }
  25% {
    transform: translate(-5px, -5px);
  }
  50% {
    transform: translate(5px, 5px);
  }
  75% {
    transform: translate(-5px, 5px);
  }
}

/* General grid animation */
.grid div {
  animation: scalePulse 6s infinite ease-in-out, subtleMove 8s infinite ease-in-out;
  will-change: transform;
}

/* Individual delay for each grid cell to create staggered effect */
.grid div:nth-child(1) { animation-delay: 0s, -0.5s; }
.grid div:nth-child(2) { animation-delay: 0.1s, -0.6s; }
.grid div:nth-child(3) { animation-delay: 0.2s, -0.7s; }
.grid div:nth-child(4) { animation-delay: 0.3s, -0.8s; }
.grid div:nth-child(5) { animation-delay: 0.4s, -0.9s; }
.grid div:nth-child(6) { animation-delay: 0.5s, -1s; }


</style>


