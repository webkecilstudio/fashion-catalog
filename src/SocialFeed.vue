<script setup lang="ts">
const looks = [
  'photo-1529139574466-a303027c1d8b',
  'photo-1539109136881-3be0616acf4b',
  'photo-1525507119028-ed4c629a60a3',
  'photo-1483985988355-763728e1935b',
  'photo-1485230895905-ec40ba36b9bc',
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
          >Gaya kalian / 05</span
        >
        <h2 class="mt-2.5 text-[clamp(30px,4vw,48px)] font-medium tracking-[-.055em]">
          Worn by you.
        </h2>
      </div>
      <a
        class="whitespace-nowrap border-b border-[#777] pb-[7px] font-mono text-[11px] font-medium uppercase tracking-[.08em]"
        href="https://instagram.com"
        target="_blank"
        rel="noreferrer"
        >Ikuti @webkecil
        <svg
          class="inline size-3.5"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="1.8"
          aria-hidden="true"
        >
          <path d="M7 17 17 7M7 7h10v10" /></svg
      ></a>
    </div>
    <div class="grid grid-cols-5 gap-3 max-[700px]:grid-cols-3 max-[700px]:gap-[7px]">
      <a
        v-for="(image, i) in looks"
        :key="image"
        class="group relative h-[220px] overflow-hidden bg-[#222] max-[700px]:h-[min(32vw,180px)] max-[700px]:nth-[n+4]:hidden"
        href="https://instagram.com"
        target="_blank"
        rel="noreferrer"
        :aria-label="`Webkecil community look ${i + 1}`"
        ><img
          class="h-full w-full object-cover transition-transform duration-300 group-hover:scale-[1.04]"
          :src="`https://images.unsplash.com/${image}?auto=format&fit=crop&w=650&q=80`"
          alt="Inspirasi outfit dari komunitas Webkecil" /><span
          class="absolute bottom-2 right-2 [text-shadow:0_1px_5px_#000]"
          ><svg
            class="size-4"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="1.8"
            aria-hidden="true"
          >
            <path d="M7 17 17 7M7 7h10v10" /></svg></span
      ></a>
    </div>
  </section>
</template>
