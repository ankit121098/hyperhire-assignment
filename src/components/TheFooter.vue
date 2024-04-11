<template>
  <section class="bg-gray-50 py-20 px-6">
    <div class="max-w-7xl mx-auto">
      <div class="md:flex flex-nowrap justify-between gap-6">
        <!-- section left -->
        <div>
          <span>
            <img src="/hyperhire_logo.svg" alt="" />
          </span>
          <div class="font-bold mt-3">
            우리는 국가의 장벽을 넘어 최고의 인재를 매칭해드립니다.
          </div>
          <div class="font-bold mt-2">010-0000-0000</div>
          <div class="font-bold">aaaaa@naver.com</div>
        </div>

        <!-- section right -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-6 py-3">
          <div
            v-for="(card, idx) in cards"
            :key="idx"
            class="bg-white shadow-card px-5 py-4 rounded-md flex flex-col"
          >
            <div class="bg-gray-200 w-fit p-2 rounded-lg">
              <img :src="card.icon" :alt="card.title" />
            </div>
            <h2 class="font-bold leading-8 mt-3">{{ card.title }}</h2>
            <div class="flex gap-2 mt-auto cursor-pointer hover:underline">
              {{ card.caption }}
              <span>
                <img src="src/assets/arrow_right_square.svg" alt="" />
              </span>
            </div>
          </div>
        </div>
      </div>

      <!-- section part 2 -->

      <div class="sm:flex space-y-8 sm:space-y-0 mt-10 gap-10">
        <!-- 1 -->
        <div class="space-y-1">
          <div class="font-bold">상호명</div>
          <div class="font-bold">하이퍼하이어</div>
          <div class="font-bold">Hyperhire India Private Limited</div>
        </div>

        <!-- 2 -->
        <div class="space-y-1">
          <div class="font-bold">대표 CEO</div>
          <div class="font-bold">김주현</div>
          <div class="font-bold">Juhyun Kim</div>
        </div>
        <!-- 3 -->
        <div class="space-y-1">
          <div class="font-bold">사업자등록번호 CIN</div>
          <div class="font-bold">427-86-01187</div>
          <div class="font-bold">U74110DL2016PTC290812</div>
        </div>
        <!-- 4 -->
        <div class="space-y-1">
          <div class="font-bold">주소 ADDRESS</div>
          <div class="font-bold">서울특별시 강남대로 479, 지하 1층 238호</div>
          <div class="font-bold">
            D-138, Street number 11, Jagjeet Nagar, North East Delhi, New Delhi,
            110053 India
          </div>
        </div>
      </div>

      <!-- copyright -->
      <div class="mt-10">
        <span class="font-bold">ⓒ 2023 Hyperhire</span>
      </div>
    </div>
  </section>
</template>

<script setup>
const cards = [
  {
    icon: "src/assets/icon-code.svg",
    title: "해외 개발자 원격 채용",
    caption: "바로가기",
    to: "/",
  },
  {
    icon: "src/assets/icon-avatar.svg",
    title: "외국인 원격 채용 (비개발)",
    caption: "바로가기",
    to: "/",
  },
  {
    icon: "src/assets/icon-kor.svg",
    title: "해외 개발자 원격 채용",
    caption: "바로가기",
    to: "/",
  },
  {
    icon: "src/assets/icon-gear.svg",
    title: "해외 개발자 원격 채용",
    caption: "바로가기",
    to: "/",
  },
];
</script>
