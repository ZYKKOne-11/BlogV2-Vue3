<template>
  <div class="px-4 py-10 text-center text-gray-700 dark:text-gray-200">
    <router-view />

    <div class="mt-20">
      <router-link to="/"> Go Back </router-link>

      <PageFooter name="NotFound" class="fixed bottom-0 mt-5" />
    </div>
  </div>
</template>
