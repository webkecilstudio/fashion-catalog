<script setup lang="ts">
const categories = [
  { name: 'Atasan', image: 'photo-1645389777532-1bc0388077fc' },
  { name: 'Bawahan', image: 'photo-1548883354-7622d03aca27' },
  { name: 'Outerwear', image: 'photo-1539533018447-63fcce2678e3' },
  { name: 'Aksesoris', image: 'photo-1590874103328-eac38a683ce7' },
]
</script>
<template>
  <section class="px-[max(6vw,24px)] py-[88px] max-[700px]:px-5 max-[700px]:py-16">
    <div
      class="mb-8 flex items-end justify-between gap-6 max-[700px]:mb-6 max-[700px]:flex-col max-[700px]:items-start"
    >
      <div>
        <span
          class="font-mono text-[11px] font-medium uppercase leading-[1.4] tracking-[.12em] text-[#a1a1aa]"
          >Cari gaya kamu / 03</span
        >
        <h2 class="mt-2.5 text-[clamp(30px,4vw,48px)] font-medium tracking-[-.055em]">
          Shop by Category
        </h2>
      </div>
    </div>
    <div class="grid grid-cols-4 gap-[14px] max-[800px]:grid-cols-2">
      <a
        v-for="(cat, i) in categories"
        :key="cat.name"
        class="group relative h-[390px] overflow-hidden bg-[#222] after:absolute after:inset-x-0 after:bottom-0 after:top-[40%] after:bg-[linear-gradient(transparent,rgba(0,0,0,.6))] max-[800px]:h-[300px] max-[480px]:h-[230px]"
        href="#new-arrivals"
        ><img
          class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-[1.04]"
          :src="`https://images.unsplash.com/${cat.image}?auto=format&fit=crop&w=1000&q=80`"
          :alt="cat.name"
        /><span
          class="absolute bottom-[66px] left-5 z-[1] font-mono text-[10px] text-[#ddd] max-[480px]:left-3.5"
          >0{{ i + 1 }} /</span
        >
        <h3
          class="absolute bottom-6 left-5 z-[1] m-0 text-2xl font-medium tracking-[-.04em] max-[480px]:left-3.5 max-[480px]:text-xl"
        >
          {{ cat.name }}
        </h3>
        <b class="absolute bottom-5 right-5 z-[1] font-normal max-[480px]:right-3.5"><svg class="size-5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M7 17 17 7M7 7h10v10" /></svg></b></a
      >
    </div>
    <div class="mt-3 flex gap-2.5">
      <a
        v-for="name in ['Wanita', 'Pria', 'Dress']"
        :key="name"
        class="flex-1 border border-[#27272a] p-4 font-mono text-[11px] uppercase"
        href="#new-arrivals"
        >{{ name }} <span class="float-right"><svg class="size-4" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M7 17 17 7M7 7h10v10" /></svg></span></a
      >
    </div>
  </section>
</template>
