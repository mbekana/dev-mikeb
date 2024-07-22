<template>
  <div class="container-footer">
    <div
      class="mx-auto px-4 sm:px-6 lg:px-8 max-w-7xl py-8 lg:py-4 lg:flex lg:items-center lg:justify-between lg:gap-x-3 !py-6"
    >
      <!--[-->
      <div
        class="lg:flex-1 flex items-center justify-center lg:justify-end gap-x-1.5 lg:order-3"
      >
        <!--[--><!--[--><a
          class="focus:outline-none focus-visible:outline-0 disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 p-1.5 text-gray-700 dark:text-gray-200 hover:text-gray-900 dark:hover:text-white hover:bg-gray-50 dark:hover:bg-gray-800 focus-visible:ring-inset focus-visible:ring-2 focus-visible:ring-primary-500 dark:focus-visible:ring-primary-400 inline-flex items-center"
          aria-label="Nuxt on X"
          href="https://go.nuxt.com/x"
          rel="noopener noreferrer"
          target="_blank"
          ><!--[--><!--[--><span
            class="i-simple-icons-x flex-shrink-0 h-5 w-5"
            aria-hidden="true"
          ></span
          ><!--]--><!--[--><!----><!--]--><!--[--><!----><!--]--><!--]--></a
        ><!--]--><!--[--><a
          class="focus:outline-none focus-visible:outline-0 disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 p-1.5 text-gray-700 dark:text-gray-200 hover:text-gray-900 dark:hover:text-white hover:bg-gray-50 dark:hover:bg-gray-800 focus-visible:ring-inset focus-visible:ring-2 focus-visible:ring-primary-500 dark:focus-visible:ring-primary-400 inline-flex items-center"
          aria-label="Nuxt on LinkedIn"
          href="https://go.nuxt.com/linkedin"
          rel="noopener noreferrer"
          target="_blank"
          ><!--[--><!--[--><span
            class="i-simple-icons-linkedin flex-shrink-0 h-5 w-5"
            aria-hidden="true"
          ></span
          ><!--]--><!--[--><!----><!--]--><!--[--><!----><!--]--><!--]--></a
        ><!--]--><!--[--><a
          class="focus:outline-none focus-visible:outline-0 disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 p-1.5 text-gray-700 dark:text-gray-200 hover:text-gray-900 dark:hover:text-white hover:bg-gray-50 dark:hover:bg-gray-800 focus-visible:ring-inset focus-visible:ring-2 focus-visible:ring-primary-500 dark:focus-visible:ring-primary-400 inline-flex items-center"
          aria-label="Nuxt on Discord"
          href="https://go.nuxt.com/discord"
          rel="noopener noreferrer"
          target="_blank"
          ><!--[--><!--[--><span
            class="i-simple-icons-discord flex-shrink-0 h-5 w-5"
            aria-hidden="true"
          ></span
          ><!--]--><!--[--><!----><!--]--><!--[--><!----><!--]--><!--]--></a
        ><!--]--><!--[--><a
          class="focus:outline-none focus-visible:outline-0 disabled:cursor-not-allowed disabled:opacity-75 flex-shrink-0 font-medium rounded-md text-sm gap-x-1.5 p-1.5 text-gray-700 dark:text-gray-200 hover:text-gray-900 dark:hover:text-white hover:bg-gray-50 dark:hover:bg-gray-800 focus-visible:ring-inset focus-visible:ring-2 focus-visible:ring-primary-500 dark:focus-visible:ring-primary-400 inline-flex items-center"
          aria-label="Nuxt on GitHub"
          href="https://go.nuxt.com/github"
          rel="noopener noreferrer"
          target="_blank"
          ><!--[--><!--[--><span class="fa fa-github" aria-hidden="true"></span
          ><!--]--><!--[--><!----><!--]--><!--[--><!----><!--]--><!--]--></a
        ><!--]--><!--]-->
      </div>
      <div class="mt-3 lg:mt-0 lg:order-2 flex items-center justify-center">
        <!--[--><!----><!--]-->
      </div>
      <div
        class="flex items-center justify-center lg:justify-start lg:flex-1 gap-x-1.5 mt-3 lg:mt-0 lg:order-1"
      >
        <!--[-->
        <p class="text-sm">
          Copyright © - {{ getCurrentYear() }}
          <a
            href="https://go.nuxt.com/license"
            rel="noopener noreferrer"
            target="_blank"
            class="hover:underline"
          >
            <!-- MIT License -->
          </a>
        </p>
        <!--]-->
      </div>
      <!--]-->
    </div>
  </div>
</template>

<script lang="ts" setup>
const getCurrentYear = () => {
  return new Date().getFullYear();
};
</script>

<style scoped>
.container-footer {
  background-color: #ba945a;
  color: #3e362e !important;
}
</style>
