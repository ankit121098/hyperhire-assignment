<template>
  <section
    class="flex flex-col justify-center bg-gradient-to-br from-sky-400 text-white to-blue-500 px-6"
  >
    <TheHeader />
    <!-- <div class="asset"></div> -->
    <div class="max-w-7xl w-full mx-auto py-10">
      <div class="grid place-items-center md:grid-cols-2 w-full">
        <div>
          <!-- details -->
          <div>
            <div
              data-aos="fade-up"
              data-aos-delay="500"
              class="bg-white text-sky-400 px-2 py-1 rounded-md font-bold relative triangle w-fit"
            >
              풀타임, 파트타임
            </div>

            <h1
              class="font-bold text-4xl lg:text-6xl mt-5"
              data-aos="fade-up"
              data-aos-duration="500"
            >
              최고의 실력을 가진 외국인 인재를 찾고 계신가요?
            </h1>
            <h3
              class="font-bold leading-8 mt-6"
              data-aos="fade-up"
              data-aos-duration="500"
            >
              법률 및 인사관리 부담없이 1주일 이내에 원격으로 채용해보세요.
            </h3>
            <!-- desktop only -->
            <p
              class="underline hidden md:!flex"
              data-aos="fade-right"
              data-aos-duration="500"
            >
              개발자가 필요하신가요?
            </p>
          </div>

          <!-- cards -->
          <!-- desktop only -->
          <div class="hidden md:!flex mb-6 mt-16 gap-3">
            <!-- 1 -->
            <div class="" data-aos="fade-up" data-aos-duration="500">
              <div class="font-bold w-fit pt-2 border-t border-white">
                평균 월 120만원
              </div>
              <div>
                임금을 해당 국가를 <br />
                기준으로 계산합니다.
              </div>
            </div>
            <!-- 2 -->
            <div data-aos="fade-up" data-aos-duration="500">
              <div class="font-bold w-fit pt-2 border-t border-white">
                최대 3회 인력교체
              </div>
              <div>
                막상 채용해보니 맞지 <br />
                않아도 걱정하지 마세요.
              </div>
            </div>
            <!-- 3 -->
            <div data-aos="fade-up" data-aos-duration="500">
              <div class="font-bold w-fit pt-2 border-t border-white">
                평균 월 120만원
              </div>
              <div>
                임금을 해당 국가를 <br />
                기준으로 계산합니다.
              </div>
            </div>
          </div>
        </div>

        <div class="">
          <div class="text-center" data-aos="fade-up" data-aos-delay="500">
            <span
              class="bg-white text-green-400 text-lg px-2 py-1 rounded-md font-bold relative triangle after:!left-10"
            >
              월 100만원
            </span>
          </div>
          <TheCarousel data-aos="fade-up" data-aos-delay="300" />
          <!-- carausel -->
        </div>
      </div>

      <!-- desktop only -->
      <div class="hidden md:!flex gap-3 mt-10">
        <div
          data-aos="fade-up"
          data-aos-duration="500"
          v-for="card in cards"
          :key="card.title"
          class="flex items-center flex-nowrap gap-3 bg-white/25 px-4 py-3 rounded-md w-56"
        >
          <div class="bg-white/40 p-1 rounded-md">
            <img :src="card.icon" class="h-6" alt="" />
          </div>
          <span class="font-bold text-white">{{ card.title }}</span>
        </div>
      </div>

      <!-- mobile only -->
      <div class="flex w-fit mt-10 md:hidden">
        <div
          v-for="text in textsMobile"
          :key="text"
          class="flex w-1/2 items-center gap-3 py-1"
        >
          <input type="checkbox" class="scale-150" :checked="true" readonly />
          <span class="font-bold text-white">{{ text }}</span>
        </div>
      </div>
      <div class="text-yellow-400 font-bold mt-4 underline md:hidden">
        개발자가 필요하신가요?
      </div>
    </div>
  </section>
</template>
<script setup>
import TheHeader from "./TheHeader.vue";
import TheCarousel from "./TheCarousel.vue";

const textsMobile = ["한국어 능력", "업무 수행 능력", "겸업 여부", "평판 조회"];

const cards = [
  {
    icon: "src/assets/hero/icon-marketing.svg",
    title: "해외 마케팅",
  },
  {
    icon: "src/assets/hero/icon-image.svg",
    title: "퍼블리셔",
  },
  {
    icon: "src/assets/hero/icon-box.svg",
    title: "캐드원(제도사)",
  },
  {
    icon: "src/assets/hero/icon-target.svg",
    title: "해외 세일즈",
  },
  {
    icon: "src/assets/hero/icon-call.svg",
    title: "해외 CS",
  },
];
</script>
<style>
.asset {
  position: absolute;
  width: 1920px;
  height: 929px;
  left: -92px;
  top: -15px;

  background: url(src/assets/overlay.png);
  mix-blend-mode: color-burn;
  opacity: 0.8;
}

.triangle::after {
  @apply content-[''] bg-white block absolute -bottom-1  left-3 w-3 h-3 rotate-45;
}
</style>
