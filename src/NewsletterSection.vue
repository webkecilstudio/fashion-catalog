<script setup lang="ts">
import { ref } from 'vue'
const email = ref('')
const submitted = ref(false)
function subscribe() { if (email.value) submitted.value = true }
</script>
<template>
  <section class="border-y border-[#27272a] px-[max(6vw,24px)] py-[88px] max-[700px]:px-5 max-[700px]:py-16" id="newsletter"><span class="font-mono text-[11px] font-medium uppercase leading-[1.4] tracking-[.12em] text-[#a1a1aa]">Kabar dari studio / 06</span><div class="mt-7 flex items-end justify-between gap-10 max-[700px]:flex-col max-[700px]:items-start"><div><h2 class="m-0 text-[clamp(44px,6vw,72px)] font-medium leading-[.98] tracking-[-.08em]">Good things,<br><i class="font-normal">occasionally.</i></h2><p class="mt-[18px] text-xs text-[#a1a1aa]">Info koleksi terbaru, cerita seru, plus penawaran spesial langsung ke email kamu.</p></div>
  <form class="grid w-[min(440px,45%)] grid-cols-[1fr_auto] border-b border-[#777] max-[700px]:w-full" @submit.prevent="subscribe"><label class="sr-only" for="email">Alamat email</label><input id="email" v-model="email" class="min-w-0 border-0 bg-transparent py-3.5 text-xs text-white outline-none" type="email" placeholder="Masukkan email kamu" required><button class="cursor-pointer border-0 bg-transparent font-mono text-[10px] uppercase" type="submit">{{ submitted ? 'Kamu sudah masuk daftar ✓' : 'Daftar yuk' }}</button><small class="col-span-full py-2.5 text-[9px] text-[#777]">Dengan mendaftar, kamu setuju dengan Kebijakan Privasi kami.</small></form></div></section>
</template>
