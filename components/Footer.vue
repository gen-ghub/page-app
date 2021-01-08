<template>
  <footer class="bg-black">
    <div class="grid grid-cols-6 text-white py-16">
      <div class="col-start-2 col-span-4 flex justify-evenly">
        <div>
          <h1 class="text-xl font-thin tracking-widest mb-4">Link</h1>
          <ul class="text-sm leading-relaxed">
            <li class="mb-2"><nuxt-link class="" to="/">Home</nuxt-link></li>
            <li class="mb-2"><nuxt-link class="" to="/Link01">News</nuxt-link></li>
            <li class="mb-2"><nuxt-link class="" to="/Link02">Entertainment</nuxt-link></li>
            <li class="mb-2"><nuxt-link class="" to="/Link03">Translation</nuxt-link></li>
            <li class="mb-2"><nuxt-link class="" to="/Link04">profile</nuxt-link></li>
            <li class="mb-2"><nuxt-link class="" to="/Link05">Blog</nuxt-link></li>
            <li class="mb-2"><nuxt-link class="" to="/Contact">Contact</nuxt-link></li>
          </ul>
        </div>
        <section>
          <h1 class="text-xl font-thin tracking-widest mb-4">COMPANY</h1>
          <ul class="text-xs leading-relaxed">
            <li class="mb-1">会社名</li>
            <li class="mb-1">東京都港区南青山5丁目11-24 グレイセス2F</li>
            <li class="mb-1">代表 山田 華子</li>
            <li class="mb-1">設立 2018年3月1日</li>
          </ul>
        </section>
        <section>
          <h1 class="text-xl font-thin tracking-widest">SNS</h1>
          <section class="flex">
            <a href="/"><img class="px-2 py-1" src="~/assets/f.png" /></a><span>|</span>
            <a href="/"><img class="px-2 py-1" src="~/assets/tw.png" /></a><span>|</span>
            <a href="/"><img class="px-2 py-1" src="~/assets/in.png" /></a>
          </section>
        </section>
      </div>
    </div>
    <div class="copy-ber flex justify-center text-white py-6">
      <p class="copyright font-thin text-sm">&copy; 2021 YAMADA HANAKO.</p>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.copy-ber {
  background-color: rgba(#1b1b1b, 1);
}
</style>
