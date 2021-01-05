<template>
  <footer class="bg-black">
    <div class="grid grid-cols-6 text-white py-16">
      <div class="col-start-2 col-span-4 flex justify-evenly">
        <section>
          <h1 class="text-xl font-thin tracking-widest mb-4">COMPANY</h1>
          <ul class="text-xs leading-relaxed">
            <li>会社名</li>
            <li>東京都港区南青山5丁目11-24 グレイセス2F</li>
            <li>代表 山田 華子</li>
            <li>設立 2018年3月1日</li>
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
