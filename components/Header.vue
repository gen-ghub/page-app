<template>
    <header class="pt-4 pb-4 w-full tracking-widest  ">
      <div class="grid sm:grid-cols-2 ">
        <div class="flex justify-evenly">
          <router-link to="/">
            <h1 class="text-xl font-medium">タイトル</h1>
          </router-link>
        </div>
        <nav>
      <ul class="lg:text-xl flex justify-evenly mr-8 h-full font-thin">
        <li>
          <nuxt-link class="tracking-widest " to="/Link01">News</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link02">Entertainment</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link03">Translation</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link04">Profile</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link05">Blog</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Contact">Contact</nuxt-link>
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

