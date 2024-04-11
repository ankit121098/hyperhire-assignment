<template>
  <q-carousel
    v-model="slide"
    swipeable
    animated
    arrows
    control-color="blue"
    infinite
    height="500px"
    class="bg-transparent w-[370px]"
  >
    <q-carousel-slide
      v-for="(card, idx) in cards"
      :key="idx"
      :name="idx"
      class=""
    >
      <div
        class="bg-white flex flex-col items-center h-full px-6 py-10 rounded-lg"
      >
        <img
          class="w-32 h-32 rounded-full"
          src="https://cdn.quasar.dev/img/mountains.jpg"
          alt=""
        />
        <div class="q-mt-md text-center text-black font-bold text-xl">
          {{ card.name }}
        </div>
        <div class="q-mt-md text-center text-blue-500 font-bold text-">
          마케팅 · {{ card.experience }}
        </div>

        <div class="flex items-center justify-center gap-3 font-bold mt-6">
          <span
            class="text-gray-600 border-2 rounded-lg block px-2 py-1 mt-0.5"
            v-for="(skill, idx) in card.skills"
            :key="skill + idx"
          >
            {{ skill }}
          </span>
        </div>
      </div>
    </q-carousel-slide>
  </q-carousel>
</template>
<script setup>
import { ref } from "vue";
const slide = ref(0);
const cards = [
  {
    name: "Abhishek Gupta",
    experience: "2y+",
    skills: [
      "트위터 관리",
      "마케팅 콘텐츠 제작",
      "트위터 관리",
      "마케팅 콘텐츠 제작",
      "트위터 관리",
    ],
  },
  {
    name: "Ankit Meena",
    experience: "3y+",
    skills: [
      "마케팅 콘텐츠 제작",
      "트위터 관리",
      "마케팅 콘텐츠 제작",
      "마케팅 콘텐츠 제작",
      "트위터 관리",
    ],
  },
  {
    name: "Ravi Prajapati",
    experience: "5y+",
    skills: [
      "트위터 관리",
      "마케팅 콘텐츠 제작",
      "트위터 관리",
      "마케팅 콘텐츠 제작",
      "트위터 관리",
    ],
  },
];
</script>
