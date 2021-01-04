<template>
  <section>
      <div class="top-news bg-gray-100 flex justify-center items-center">
        <h1 class="text-2xl font-light tracking-widest">NEWS</h1>
      </div>
      <section class=" w-screen grid grid-cols-8 gap-6 py-20">
        <div class="col-start-2 col-span-6 ">
          <div class="flex justify-center items-center space-x-6">
            <ul>
              <li class="mb-4"><img class="" src="~/assets/live.jpg" /></li>
              <li class="mb-1"><p class="text-xs">March 25, 2020</p></li>
              <li class="mb-2"><p class="text-xl">タイトル</p></li>
              <li class="mb-4">
                <p class="font-thin leading-relaxed">〇〇アーティストのライブの運営管理<br>
                  Newsとして表示したい内容の文章入力<br>
                  Newsとして表示したい内容の文章入力<br>
                  Newsとして表示したい内容の文章入力
                </p></li>
                <li><nuxt-link to="/" class="p-2 rounded text-black hover:bg-gray-100  transition duration-700">記事のリンク</nuxt-link></li>
            </ul>
            <ul>
              <li class="mb-4"><img class="" src="~/assets/e.jpg" /></li>
              <li class="mb-1"><p class="text-xs">March 25, 2020</p></li>
              <li class="mb-2"><p class="text-xl">タイトル</p></li>
              <li class="mb-4">
                <p class="font-thin leading-relaxed">〇〇を翻訳させていただきました。<br>
                  Newsとして表示したい内容の文章入力<br>
                  Newsとして表示したい内容の文章入力<br>
                  Newsとして表示したい内容の文章入力
                </p></li>
                <li><nuxt-link to="/" class="p-2 rounded text-black hover:bg-gray-100  transition duration-700">記事のリンク</nuxt-link></li>
            </ul>
            <ul>
              <li class="mb-4"><img class="" src="~/assets/pc.jpg" /></li>
              <li class="mb-1"><p class="text-xs">March 25, 2020</p></li>
              <li class="mb-2"><p class="text-xl">タイトル</p></li>
              <li class="mb-4">
                <p class="font-thin leading-relaxed">週間東洋経済に在宅ワークについて取材<br>
                  Newsとして表示したい内容の文章入力<br>
                  Newsとして表示したい内容の文章入力<br>
                  Newsとして表示したい内容の文章入力
                </p></li>
                <li><nuxt-link to="/" class="p-2 rounded text-black hover:bg-gray-100  transition duration-700">記事のリンク</nuxt-link></li>
            </ul>
          </div>
        </div>
      </section>
          <div class="flex justify-center items-center mb-20">
            <h1 class="col-start-5 col-span-1 border border-blue-900 px-12 py-2 rounded text-black hover:bg-gray-400  transition duration-700">read more</h1>
          </div>
    </section>
</template>
<style lang="scss" scoped>
.top-news{
  height: 15vh;
}

img{
  height: 400px;
  width: 400px;
}
</style>
