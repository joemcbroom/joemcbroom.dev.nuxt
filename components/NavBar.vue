<script setup>
const routes = [
  { name: "About", path: "/about" },
  { name: "Resume", path: "/resume" },
  { name: "Contact", path: "/contact" },
];
</script>

<template>
  <nav class="relative bg-teal-500">
    <ContainerWrap>
      <!-- center image in nav -->
      <NuxtLink
        to="/"
        class="absolute h-24 left-1/2 transform -translate-x-1/2"
      >
        <img
          src="~/assets/img/joemcbroomlogo.png"
          alt="Joe McBroom Logo"
          class="object-contain h-full"
        />
      </NuxtLink>

      <div class="flex items-center justify-center gap-4 h-24 w-full">
        <div v-for="route in routes" :key="route.name" class="last:ml-auto">
          <NuxtLink v-if="route.name !== 'Home'" :to="route.path">
            {{ route.name }}
          </NuxtLink>
        </div>
      </div>
    </ContainerWrap>
  </nav>
</template>
