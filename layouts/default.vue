<template>
  <section>
    <main>
      <Nuxt />
    </main>
    <Footer />
  </section>
</template>

<script>
  import Footer from "@/components/Footer.vue";
export default {
  components: {
    Footer
  }
};
</script>

<style lang="scss" scoped>

  .page-enter-active,
  .page-leave-active {
    transition: 0.5s cubic-bezier(1, 0.25, 0.25, 1);
  }
  .page-enter,
  .page-leave-active {
    opacity: 0;
    transform: translate(0, 30px);
  }

main{
  height: 100%;
}
</style>
