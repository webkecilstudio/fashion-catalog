<script setup lang="ts">
import AnnouncementBar from './AnnouncementBar.vue'
import SiteHeader from './SiteHeader.vue'
import HeroSection from './HeroSection.vue'
import ProductSection from './ProductSection.vue'
import CategorySection from './CategorySection.vue'
import CollectionSection from './CollectionSection.vue'
import BrandStory from './BrandStory.vue'
import SocialFeed from './SocialFeed.vue'
import NewsletterSection from './NewsletterSection.vue'
import SiteFooter from './SiteFooter.vue'
</script>

<template>
  <div class="min-w-[360px] bg-[#050505] font-['Inter',sans-serif] text-white antialiased">
    <AnnouncementBar />
    <SiteHeader />
    <main>
      <HeroSection />
      <ProductSection kind="new" />
      <CategorySection />
      <CollectionSection />
      <ProductSection kind="best" />
      <BrandStory />
      <SocialFeed />
      <NewsletterSection />
    </main>
    <SiteFooter />
  </div>
</template>
