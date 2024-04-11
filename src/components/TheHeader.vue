<template>
  <header class="">
    <div
      class="flex items-center justify-between py-3 font-bold max-w-7xl mx-auto"
    >
      <img src="src/assets/logo.svg" alt="" />

      <div class="hidden md:!flex gap-10">
        <button class="flex items-center gap-1">
          채용
          <img src="src/assets/arrow_down.svg" alt="" />

          <q-menu>
            <q-list style="min-width: 100px">
              <q-item clickable dense class="py-2 font-bold" v-close-popup>
                <q-item-section>채용</q-item-section>
              </q-item>
              <q-item clickable dense class="py-2" v-close-popup>
                <q-item-section>해외 개발자 원격 채용</q-item-section>
              </q-item>
              <q-item clickable dense class="py-2" v-close-popup>
                <q-item-section>외국인 원격 채용 (비개발 직군)</q-item-section>
              </q-item>
              <q-item clickable dense class="py-2" v-close-popup>
                <q-item-section>한국어 가능 외국인 채용</q-item-section>
              </q-item>
            </q-list>
          </q-menu>
        </button>

        <button class="block ml-">해외 개발자 활용 서비스</button>
      </div>

      <button
        class="outline-none border-none bg-white rounded-md font-bold text-blue-600 px-6 py-2"
      >
        문의하기
      </button>
    </div>
  </header>
</template>

<script setup>
const test = "";
</script>
