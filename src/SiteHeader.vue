<script setup lang="ts">
import { ref } from 'vue'
const menuOpen = ref(false)
</script>
<template>
  <header
    class="relative z-[2] flex h-[76px] items-center justify-between border-b border-[#27272a] px-[6vw] max-[760px]:h-[66px] max-[760px]:px-5"
  >
    <a class="text-[18px] font-bold tracking-[-.08em] max-[760px]:text-base" href="#home"
      >WEBKECIL<span class="ml-[3px] align-top font-mono text-[10px]">®</span></a
    >
    <nav
      :class="[
        menuOpen ? 'max-[760px]:flex' : 'max-[760px]:hidden',
        'flex items-center gap-8 font-mono text-[11px] uppercase tracking-[.04em] max-[760px]:absolute max-[760px]:left-0 max-[760px]:right-0 max-[760px]:top-[65px] max-[760px]:flex-col max-[760px]:items-start max-[760px]:border-b max-[760px]:border-[#27272a] max-[760px]:bg-[#050505] max-[760px]:p-6',
      ]"
    >
      <a href="#home">Beranda</a><a href="#new-arrivals">Belanja</a><a href="#collection">Koleksi</a
      ><a href="#story">Cerita Kami</a>
    </nav>
    <div
      class="flex items-center gap-5 font-mono text-[11px] uppercase tracking-[.04em] max-[760px]:gap-3"
    >
      <button class="cursor-pointer border-0 bg-transparent text-xl" aria-label="Cari">⌕</button>
      <a class="max-[760px]:hidden" href="#newsletter" aria-label="Akun">Akun</a>
      <a href="#new-arrivals">Keranjang <span>(0)</span></a>
      <button
        class="hidden cursor-pointer border-0 bg-transparent max-[760px]:block"
        aria-label="Buka navigasi"
        @click="menuOpen = !menuOpen"
      >
        {{ menuOpen ? '×' : '☰' }}
      </button>
    </div>
  </header>
</template>
