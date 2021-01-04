<template>
  <section>
    <TopImage />
    <News />
    <Work />
  </section>
</template>

<script>
import TopImage from '@/components/TopImage.vue'
import News from '@/components/News.vue'
import Work from '@/components/Work.vue'

export default {
  components: {
    TopImage,
    News,
    Work
  },
}

</script>

<style lang="scss" scoped>

</style>
