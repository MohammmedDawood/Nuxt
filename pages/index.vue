<template>
  <div>
    <div class="container">
      <Hero />
      <LargeCardDisplay
        v-for="cardinfo in largecardinfo"
        :key="'lg' + cardinfo.id"
        :cardssection="cardinfo"
      />
      <SmallCardDisplay
        v-for="cardinfo in smallcardinfo"
        :key="'sm' + cardinfo.id"
        :cardssection="cardinfo"
      />
    </div>
  </div>
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data.js'
export default {
  data() {
    return {
      largecardinfo: largeCardSections,
      smallcardinfo: smallCardSections,
    }
  },
}
</script>

<style></style>
