<template>
    <header class="fixed z-20 pt-10 pb-8 w-full  text-white tracking-widest font-thin font-serif">
      <div class="grid sm:grid-cols-2 ">
        <div class="ml-8 w-1/4">
          <router-link to="/">
            <h1 class="text-4xl">タイトル</h1>
          </router-link>
        </div>
        <nav>
      <ul class="lg:text-xl flex content-center mr-8 h-full">
        <li>
          <nuxt-link class="tracking-widest font-thin " to="/Link01"></nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest font-thin " to="/Link02"></nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest font-thin " to="/Link03"></nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest font-thin " to="/Contact">お問い合わせ</nuxt-link>
        </li>
      </ul>
    </nav>
      </div>
    </header>
</template>

<script>

</script>

<style lang="scss" scoped>

</style>

