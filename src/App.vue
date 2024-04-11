<template>
  <router-view />
</template>

<script setup>
import Aos from "aos";
import "aos/dist/aos.css";

defineOptions({
  name: "App",
});

Aos.init();
</script>
