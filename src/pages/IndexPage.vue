<template>
  <q-page>
    <HeroSection />
    <TheFooter />
  </q-page>
</template>

<script setup>
import TheFooter from "src/components/TheFooter.vue";
import HeroSection from "src/components/HeroSection.vue";

defineOptions({
  name: "IndexPage",
});
</script>
