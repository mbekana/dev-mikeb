<template>
  <header class="hero-bg h-screen flex items-center justify-center relative">
    <div class="container mx-auto relative">
      <!-- Coordinates and Date -->
      <div
        id="coordinates"
        class="coordinates absolute top-0 right-0 mt-4 mr-4 flex flex-row md:flex-row items-start md:items-center justify-between p-2 rounded text-[#ab8867]"
      >
        <p class="text-sm md:text-sm mb-2 md:mb-0">
          {{ getDateInUTCString() }}
        </p>
        <div class="text-sm md:text-base">
          <p id="coord-x">X: {{ xVal }}</p>
          <p id="coord-y">Y: {{ yVal }}</p>
        </div>
      </div>

      <!-- Main Content -->
      <div class="text-center fade-in hero-text">
        <h1 class="text-6xl font-bold">Milkias Bekana</h1>
        <p class="mt-4 text-2xl">Full-Stack Developer</p>
        <p class="mt-2 text-xl">
          Specializing in React, Angular, Vuejs, Nux.js, Next.js, Tailwind CSS,
          and Spring Boot.
        </p>
        <div class="mt-6 flex justify-center space-x-4">
          <a
            href="https://www.linkedin.com/in/milkias-bekana/"
            target="_blank"
            class="text-3xl hover:text-blue-300 transition duration-300 transform hover:scale-110"
          >
            <i class="fab fa-linkedin"></i>
          </a>
          <a
            href="https://github.com/mbekana"
            target="_blank"
            class="text-3xl hover:text-gray-300 transition duration-300 transform hover:scale-110"
          >
            <i class="fab fa-github"></i>
          </a>
          <a
            href="https://www.upwork.com/freelancers/milkiasb"
            target="_blank"
            rel="noopener noreferrer"
            class="text-3xl text-white hover:text-gray-300 transition duration-300 transform hover:scale-110"
          >
            <fa :icon="['fab', 'upwork']" />
          </a>
        </div>
        <nav class="mt-6">
          <a
            href="#about"
            class="bg-[#ab8867] hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full mx-2 transition duration-300"
            >About</a
          >
          <a
            href="#portfolio"
            class="bg-[#ab8867] hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full mx-2 transition duration-300"
            >Portfolio</a
          >
          <a
            href="#contact"
            class="bg-[#ab8867] hover:bg-blue-700 text-white font-bold py-2 px-4 rounded-full mx-2 transition duration-300"
            >Contact</a
          >
        </nav>
        <div class="mt-6 resume-and-contact">
          <a
            href="Milkias-Bekana-Resume-J24.pdf"
            class="bg-transparent border-2 border-green-500 text-green-500 hover:bg-green-500 hover:text-white font-bold py-2 px-4 rounded-full mx-2 transition duration-300"
            download
            >Download Resume</a
          >
        </div>
      </div>
    </div>
    <div class="flex flex-row justify-start">
      <p>Scroll To Bottom</p>
    </div>
  </header>
  <div ref="cursor" class="pointer"></div>
  <div ref="cursor2" class="pointer2"></div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const xVal = ref(0);
const yVal = ref(0);

const cursor = ref(null);
const cursor2 = ref(null);

onMounted(() => {
  const updateCursor = (e) => {
    if (cursor.value && cursor2.value) {
      cursor.value.style.left = `${e.clientX}px`;
      cursor.value.style.top = `${e.clientY}px`;
      cursor2.value.style.left = `${e.clientX}px`;
      cursor2.value.style.top = `${e.clientY}px`;
    }
    xVal.value = e.clientX;
    yVal.value = e.clientY;
  };

  document.addEventListener("mousemove", updateCursor);
});

const getDateInUTCString = () => {
  const date = new Date();
  return date.toUTCString();
};
</script>
<style scoped>
.pointer {
  position: fixed;
  width: 50px;
  height: 50px;
  border: 1px solid #c6c6c6;
  left: 0;
  top: 0;
  pointer-events: none;
  transform: translate(-50%, -50%);
  transition: 0.1s;
  border-radius: 50%;
}

.pointer2 {
  position: fixed;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  border: 1px solid #c6c6c6;
  background-color: green;
  left: 0;
  top: 0;
  pointer-events: none;
  transform: translate(-50%, -50%);
}

.coordinates {
  position: fixed;
  margin-left: auto;
  top: 0;
  left: 0;
  /* padding: 5px;
  border-radius: 5px;
  pointer-events: none;
  z-index: 9999;
  color: #ab8867;

  width: 100%;
  max-width: 600px;
  display: flex;
  justify-content: space-between;
  align-items: center; */
}

.hero-bg {
  position: relative;
  z-index: 0;
}

.hero-text {
  color: #ab8867;
}

.hero-bg::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: #3e362e;
  z-index: -1;
}

.hero-bg::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

.fade-in {
  animation: fadeIn 2s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.section-content {
  max-width: 1200px;
  margin: auto;
  text-align: center;
}

.rounded-full {
  border: 4px solid rgba(224, 231, 233, 0.7);
}

.horizontal-line {
  border-bottom: 2px solid rgba(224, 231, 233, 0.5);
  width: 60%;
  margin: 20px auto;
}
</style>
