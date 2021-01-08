<template>
  <div>
    <div class="grid grid-cols-2 h-full">
      <section class="col-span-2 lg:col-span-1 lg:col-start-1 bg-gray-200 flex justify-center">
        <div class="flex flex-col items-center">
          <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-4">
            Be free within constraints
          </h2>
          <h1 class="tracking-widest text-xl font-extralight mb-10">ACTRESS</h1>
          <div
            class="leading-loose text-sm flex flex-col items-center font-thin tracking-widest mb-16"
          >
            <p class="">エンタメの説明文エンタメの説明文</p>
            <p>わからないことは、ワクワクする。</p>
            <p>積み重ねてきた過去の経験。感情の昇華。</p>
            <p>DETOXでもあり、新しい自分との出逢いである</p>
            <p>俳優という仕事を通して自分自身と向き合い</p>
            <p class="mb-8">
              宝物を探しながら、人生をおもしろく、豊かにしていく。
            </p>
            <p>その人の魅力は「その人らしさ」</p>
            <p class="mb-8">唯一無二。</p>
            <p>誰かの「らしさ」-生き方を変えるかもしれない</p>
            <p>魅力的な作品、世界の中を生きることで伝えていく。</p>
          </div>
          <nuxt-link to="/Link02" class="mb-32">
            <button
              class="p-2 rounded text-black hover:bg-blue-900 hover:text-white transition duration-700"
            >
              Entertainment
            </button>
          </nuxt-link>
        </div>
      </section>
      <div class="col-span-2 lg:col-start-2 bg-green-200">
        <img class="h-full w-full object-cover" src="~/assets/leg.jpg" />
      </div>
      <div class="hidden lg:contents lg:col-span-1 lg:col-start-1 bg-green-200">
        <img class="h-full w-full object-cover" src="~/assets/sun.jpg" />
      </div>
      <section class="col-span-2 lg:col-span-1 lg:col-start-2 bg-gray-200 flex justify-center items-center">
        <div class="flex flex-col items-center">
          <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-4">
            Happiness comes from within
          </h2>
          <h1 class="tracking-widest text-xl font-extralight mb-10">
            COUNSELOR
          </h1>
          <div
            class="leading-loose text-sm flex flex-col items-center font-thin tracking-widest mb-16"
          >
            <p class="">翻訳家の説明文翻訳家の説明文</p>
            <p>わからないことは、ワクワクする。</p>
            <p>積み重ねてきた過去の経験。感情の昇華。</p>
            <p>DETOXでもあり、新しい自分との出逢いである</p>
            <p>俳優という仕事を通して自分自身と向き合い</p>
            <p class="mb-8">
              宝物を探しながら、人生をおもしろく、豊かにしていく。
            </p>
            <p>その人の魅力は「その人らしさ」</p>
            <p class="mb-8">唯一無二。</p>
            <p>誰かの「らしさ」-生き方を変えるかもしれない</p>
            <p>魅力的な作品、世界の中を生きることで伝えていく。</p>
          </div>
          <nuxt-link to="/Link03" class="mb-32">
            <button
              class="p-2 rounded text-black hover:bg-blue-900 hover:text-white transition duration-700"
            >
              Translation
            </button>
          </nuxt-link>
        </div>
      </section>
      <div class=" col-span-2 lg:col-start-1 lg:hidden bg-green-200">
        <img class="h-full w-full object-cover" src="~/assets/sun.jpg" />
      </div>
      <section class="col-span-2 lg:col-span-1 lg:col-start-1 bg-gray-200 flex justify-center items-center">
        <div class="flex flex-col items-center">
          <h2 class="mb-4">華子</h2>
          <h1 class="text-3xl tracking-widest font-semibold mb-20">
            YAMADA HANAKO
          </h1>
          <div>
            <nuxt-link to="/Link04">
              <button
                class="tracking-widest text-lg p-2 rounded text-black hover:bg-blue-900 hover:text-white transition duration-700"
              >
                profile
              </button>
            </nuxt-link>
            <nuxt-link to="/Link05">
              <button
                class="tracking-widest text-lg p-2 rounded text-black hover:bg-blue-900 hover:text-white transition duration-700"
              >
                blog
              </button>
            </nuxt-link>
          </div>
        </div>
      </section>
      <div class="col-span-2 lg:col-start-2 bg-green-200">
        <img class="user-img object-cover" src="~/assets/woman2.jpg" />
      </div>
    </div>
    <div class="flex justify-center items-center h-screen">
      <div>
        <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-12">
          Just the way you are
        </h2>
        <div class="leading-loose flex flex-col items-center font-thin tracking-widest mb-16">
          <p>自分らしくのびのびと</p>
          <p>表現することをやめず</p>
          <p>輝くその才能が</p>
          <p>後世に引き継がれますように</p>
        </div>
      </div>
    </div>
  </div>
</template>
<style lang="scss" scoped>
.user-img {
  height: 820px;
  width: 100%;
}
</style>
