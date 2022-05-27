<template>
  <div class="h-8 leading-8 my-4">
    <input
      v-model.trim="name"
      type="text"
      h="full"
      p="x-2"
      bg="gray-100"
      text="gray-600"
      outline="none"
    />
    <button
      class="rounded"
      h="full"
      m="l-4"
      p="x-2"
      bg="green-500"
      text="white lg"
    >
      Go <IconMdiGoogleDownasaur class="animate-bounce align-middle" />
    </button>
  </div>
</template>
