<template>

  <div class="w-full min-h-screen bg-black">

    <!-- Navigation Bar -->
    <section class="max-w-screen-lg mx-auto p-4 flex justify-between items-center">

      <NuxtLink to="/" class="z-10 text-3xl font-semibold text-gray-300">S</NuxtLink>

      <div class="absolute md:static z-0 md:z-10 flex flex-col md:flex-row items-center gap-2 md:gap-10 min-h-[50vh] md:min-h-fit left-0 w-full md:w-auto font-extralight text-white duration-500 bg-black" :class="showDropdownMenu ? 'top-[9%]' : 'top-[-100%]'">
        <NuxtLink to="/dashbaord" class="glow-text">Dashboard</NuxtLink>
        <NuxtLink to="/showcases" class="glow-text">Showcases</NuxtLink>
        <NuxtLink to="/philosophy" class="glow-text">Philosophy</NuxtLink>
        <NuxtLink to="/about-us" class="glow-text">About Us</NuxtLink>
      </div>

      <div class="z-10 flex items-center gap-3">
        <NuxtLink to="/sign-in" class="border border-gray-300 text-gray-300 rounded-lg py-1 px-2 hover:cursor-pointer glow-on-hover"> Sign in </NuxtLink>
        <button @click="toggleDropdownMenu()" name="menu" class="text-white cursor-pointer md:hidden duration-500">
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="white" stroke-width="3" x="0px" y="0px" width="20" height="20" viewBox="0 0 50 50">
            <path :d="showDropdownMenu
            ? 'M 5,5 L 45,45 M 45,5 L 5,45'
            : 'M 5 9 L 5 11 L 45 11 L 45 9 L 5 9 z M 5 24 L 5 26 L 45 26 L 45 24 L 5 24 z M 5 39 L 5 41 L 45 41 L 45 39 L 5 39 z'"/>
          </svg>
        </button>
      </div>

    </section>


  <div class="max-w-screen-lg mx-auto text-center p-4 pt-24">
    <p class="font-extrabold tracking-tight text-gray-200 text-5xl">Symmetry Engineering Firm.</p>
    <p class="mt-4 mb-8 sm:px-16 xl:px-48 text-gray-400">
    Specialized in an array of engineering and software solutions. Cross-platform software, systems design, cloud infrastructure and services, real-time electronic and embedded systems. </p>
  </div>

  <div class="max-w-screen-lg mx-auto text-center">
    <a href="tg://resolve?domain=symmetryteam" class="p-2 px-3 rounded-lg text-white glow-animation">
      Telegram Direct Message
    </a>
  </div>

  </div>

</template>

<script setup>

const showDropdownMenu = ref(false);
function toggleDropdownMenu() {
  showDropdownMenu.value = !showDropdownMenu.value;
}

</script>


<style scoped>
@keyframes glow {
    0%, 100% {
        outline: 2px solid rgba(255, 255, 255, 0.2);
        box-shadow: 0 0 8px rgba(255, 255, 255, 0.5), 0 0 10px rgba(255, 255, 255, 0.3), inset 0 0 4px rgba(255, 255, 255, 0.2);
    }
    50% {
        outline: 2px solid rgba(255, 255, 255, 0.6);
        box-shadow: 0 0 12px rgba(255, 255, 255, 0.7), 0 0 20px rgba(255, 255, 255, 0.5), inset 0 0 8px rgba(255, 255, 255, 0.4);
    }
}

.glow-animation {
    animation: glow 2s ease-in-out infinite;
    position: relative; /* Ensure the glow is positioned correctly relative to the parent */
}

.glow-text:hover {
    color: #fff; /* Optional: change text color on hover */
    text-shadow: 
        0 0 8px rgba(255, 255, 255, 0.8),
        0 0 10px rgba(255, 255, 255, 0.6),
        0 0 12px rgba(204, 169, 44, 0.5); /* This color can be adjusted to fit your design */
    transition: text-shadow 0.3s ease-in-out;
}

/* Additional styles to enhance visibility and interaction */
.glow-text {
    transition: text-shadow 0.3s ease-in-out; /* Smooth transition for mouse enter and leave */
    cursor: pointer; /* Indicates that the element is interactive */
}

.glow-on-hover {
    position: relative; /* Ensure the glow is positioned correctly relative to the parent */
    outline: 2px solid rgba(255, 255, 255, 0.2);
    box-shadow: 0 0 8px rgba(255, 255, 255, 0.2), 0 0 10px rgba(255, 255, 255, 0.1), inset 0 0 4px rgba(255, 255, 255, 0.1);
    transition: outline 0.3s ease-in-out, box-shadow 0.3s ease-in-out; /* Smooth transition */
}

.glow-on-hover:hover {
    outline: 2px solid rgba(255, 255, 255, 0.6);
    box-shadow: 0 0 12px rgba(255, 255, 255, 0.7), 0 0 20px rgba(255, 255, 255, 0.5), inset 0 0 8px rgba(255, 255, 255, 0.4);
}

</style>
