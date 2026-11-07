<script setup lang="ts">
import { computed } from 'vue'
const props = defineProps<{ kind: 'new' | 'best' }>()
const isNew = computed(() => props.kind === 'new')
const products = isNew.value
  ? [
      {
        name: 'Kemeja Katun Rapi',
        price: '$128',
        tag: 'NEW',
        image: 'photo-1598554747436-c9293d6a588f',
      },
      {
        name: 'Celana Pleats Santai',
        price: '$168',
        tag: 'NEW',
        image: 'photo-1688535823258-9927ab196d34',
      },
      {
        name: 'Knitwear Soft Form',
        price: '$148',
        tag: 'NEW',
        image: 'photo-1576566588028-4147f3842f27',
      },
      {
        name: 'Tote Bag Kulit Studio',
        price: '$210',
        tag: 'NEW',
        image: 'photo-1590874103328-eac38a683ce7',
      },
    ]
  : [
      {
        name: 'Coat Andalan',
        price: '$320',
        tag: 'FAVORIT',
        image: 'photo-1539533018447-63fcce2678e3',
      },
      {
        name: 'Celana Tailored Relaxed',
        price: '$178',
        tag: 'FAVORIT',
        image: 'photo-1517445312882-bc9910d016b7',
      },
      {
        name: 'Tank Top Rib Harian',
        price: '$68',
        tag: 'FAVORIT',
        image: 'photo-1551488831-00ddcb6c6bd3',
      },
      {
        name: 'Tas Kulit Klasik',
        price: '$240',
        tag: 'FAVORIT',
        image: 'photo-1584917865442-de89df76afd3',
      },
    ]
</script>
<template>
  <section
    class="px-[max(6vw,24px)] py-[88px] max-[700px]:px-5 max-[700px]:py-16"
    :id="isNew ? 'new-arrivals' : 'best-sellers'"
  >
    <div
      class="mb-8 flex items-end justify-between gap-6 max-[700px]:mb-6 max-[700px]:flex-col max-[700px]:items-start"
    >
      <div>
        <span
          class="font-mono text-[11px] font-medium uppercase leading-[1.4] tracking-[.12em] text-[#a1a1aa]"
          >{{ isNew ? 'Baru datang / 01' : 'Paling disukai / 02' }}</span
        >
        <h2 class="mt-2.5 text-[clamp(30px,4vw,48px)] font-medium tracking-[-.055em]">
          {{ isNew ? 'New Arrivals' : 'Best Sellers' }}
        </h2>
      </div>
      <a
        class="whitespace-nowrap border-b border-[#777] pb-[7px] font-mono text-[11px] font-medium uppercase tracking-[.08em]"
        href="#collection"
        >Lihat semua <svg class="inline size-3.5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M7 17 17 7M7 7h10v10" /></svg></a
      >
    </div>
    <div
      class="grid grid-cols-4 gap-4 max-[900px]:grid-cols-2 max-[900px]:gap-x-3 max-[900px]:gap-y-[26px]"
    >
      <article v-for="(product, i) in products" :key="product.name" class="group">
        <div
          class="relative h-[420px] overflow-hidden bg-[#181818] max-[900px]:h-[min(110vw,520px)]"
        >
          <img
            class="h-full w-full object-cover transition-transform duration-500 group-hover:scale-[1.035]"
            :src="`https://images.unsplash.com/${product.image}?auto=format&fit=crop&w=850&q=80`"
            :alt="product.name"
            :style="{ objectPosition: i === 1 ? 'center' : '50% 35%' }"
          /><span
            class="absolute left-3 top-3 bg-[#f4f4f4] px-[9px] py-[7px] font-mono text-[9px] tracking-[.05em] text-[#111]"
            >{{ product.tag }}</span
          ><button
            class="absolute bottom-3 left-3 right-3 translate-y-[5px] cursor-pointer border-0 bg-white p-[13px] text-left font-mono text-[10px] uppercase text-[#111] opacity-0 transition duration-200 group-hover:translate-y-0 group-hover:opacity-100 focus:translate-y-0 focus:opacity-100 max-[900px]:bottom-2 max-[900px]:left-2 max-[900px]:right-2 max-[900px]:translate-y-0 max-[900px]:p-2.5 max-[900px]:opacity-100"
          >
            Lihat cepat <span class="float-right"><svg class="size-3.5" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8" aria-hidden="true"><path d="M7 17 17 7M7 7h10v10" /></svg></span>
          </button>
        </div>
        <div class="mt-3.5 flex justify-between gap-2">
          <h3 class="text-xs font-normal">{{ product.name }}</h3>
          <span class="whitespace-nowrap text-xs text-[#ccc]">{{ product.price }}</span>
        </div>
        <div class="mt-2.5 flex gap-1.5">
          <i class="size-2.5 rounded-full bg-[#c4b8a6]"></i
          ><i class="size-2.5 rounded-full bg-[#3d3b38]"></i
          ><i class="size-2.5 rounded-full bg-[#ddd]"></i>
        </div>
      </article>
    </div>
  </section>
</template>
