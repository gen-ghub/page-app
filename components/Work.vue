<template>
  <div>
    <div class="grid grid-cols-2 h-full">
      <section class="col-span-2 lg:col-span-1 lg:col-start-1 bg-gray-200 flex justify-center">
        <div class="flex flex-col items-center enterme-wrapper">
          <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-4 ">
            Be free within constraints
          </h2>
          <h1 class="tracking-widest text-xl font-extralight mb-10">ENTERTAINMENT</h1>
          <div
            class="leading-loose text-sm flex flex-col items-center font-thin tracking-widest mb-16 enterme-text"
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
          <nuxt-link to="/Contact" class="mb-32 contact-btn">
            <button
              class="w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black  hover:bg-gray-900 hover:text-white transition duration-700"
            >
              Contact
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
        <div class="flex flex-col items-center trans-wrapper">
          <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-4">
            Happiness comes from within
          </h2>
          <h1 class="tracking-widest text-xl font-extralight mb-10">
            TRANSLATION
          </h1>
          <div
            class="leading-loose text-sm flex flex-col items-center font-thin tracking-widest mb-16 trans-text"
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
          <nuxt-link to="/Contact" class="mb-32 contact-btn">
            <button
              class="w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black  hover:bg-gray-900 hover:text-white transition duration-700"
            >
              Contact
            </button>
          </nuxt-link>
        </div>
      </section>
      <div class=" col-span-2 lg:col-start-1 lg:hidden bg-green-200">
        <img class="h-full w-full object-cover" src="~/assets/sun.jpg" />
      </div>
      <section class="col-span-2 lg:col-span-1 lg:col-start-1 bg-gray-200 flex justify-center items-center profile-wrapper">
        <div class="flex flex-col items-center profile-main">
          <h2 class="mb-4">華子</h2>
          <h1 class="text-3xl tracking-widest font-semibold mb-20">
            YAMADA HANAKO
          </h1>
          <div>
            <nuxt-link to="/Link04">
              <button
                class="tracking-widest text-lg w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black  hover:bg-gray-900 hover:text-white transition duration-700"
              >
                profile
              </button>
            </nuxt-link>
            <nuxt-link to="/Link05">
              <button
                class="tracking-widest text-lg w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black  hover:bg-gray-900 hover:text-white transition duration-700"
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
    <div class="flex justify-center items-center h-screen word-wrapper">
      <div class="">
        <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-12">
          Just the way you are
        </h2>
        <div class="leading-loose flex flex-col items-center font-thin tracking-widest mb-16 word-text">
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
@media screen and (max-width: 1024px){
  .user-img {
  height: 600px;
}
.enterme-wrapper{
  h2{
    font-size: 40px;
    margin-top: 40px;
  }
  .enterme-text{
    margin-bottom: 30px;
}
}
.trans-wrapper{
  h2{
    font-size: 35px;
    margin-top: 40px;
  }
  .trans-text{
    margin-bottom: 30px;
  }
}

.contact-btn{
  margin-bottom: 40px;
}
.word-wrapper{
  height: 70vh;
  h2{
    margin-top: 40px;
  }
}
}
@media screen and (max-width: 768px){
.profile-wrapper{
  .profile-main{
    margin: 20vh 0;
  }
}
}
@media screen and (max-width: 425px){
  .user-img {
  height: 380px;
}
  .enterme-wrapper{
  h2{
    font-size: 30px;
    margin-top: 40px;
  }
  h1{
    font-size: 16px;
    margin-bottom: 30px;
  }
  .enterme-text{
    margin-bottom: 30px;
    .mb-8{
      margin-bottom: 10px;
    }
    p{
      font-size: 12px;
    }
}
}
.trans-wrapper{
  h2{
    font-size: 30px;
    margin-top: 40px;
  }
  h1{
    font-size: 16px;
    margin-bottom: 30px;
  }
  .trans-text{
    margin-bottom: 30px;
    .mb-8{
      margin-bottom: 10px;
    }
    p{
      font-size: 12px;
    }
  }
}
.profile-wrapper{
  .profile-main{
    margin: 15vh 0;
  }
}
.contact-btn{
  margin-bottom: 30px;
}
.word-wrapper{
  height: 60vh;
  h2{
    margin-top: 40px;
    font-size: 38px;
  }
}
}
@media screen and (max-width: 375px){
  .enterme-wrapper{
  h2{
    font-size: 25px;
    margin-top: 30px;
    margin-bottom: 10px;
  }
  h1{
    font-size: 14px;
    margin-bottom: 25px;
  }
  .enterme-text{
    margin-bottom: 20px;
    p{
      font-size: 10px;
    }
}
}
.trans-wrapper{
  h2{
    font-size: 25px;
    margin-top: 30px;
  }
  h1{
    font-size: 14px;
    margin-bottom: 25px;
  }
  .trans-text{
    margin-bottom: 20px;
    .mb-8{
      margin-bottom: 10px;
    }
    p{
      font-size: 10px;
    }
  }
}
.contact-btn{
  font-size: 14px;
}
.profile-wrapper{
  .profile-main{
    margin: 10vh 0;
    h1{
      font-size: 25px;
      margin-bottom: 40px;
    }
  }
}
.word-wrapper{
  height: 50vh;
  h2{
    margin-top: 40px;
  }
  .word-text{
    font-size: 14px;
  }
}
}
@media screen and (max-width: 320px){
  .trans-wrapper{
  h2{
    font-size: 20px;
    margin-top: 25px;
    margin-bottom: 15px;
  }
  h1{
    font-size: 13px;
    margin-bottom: 20px;
  }
}
.profile-wrapper{
  .profile-main{
    h1{
      font-size: 20px;
    }
    p{
      font-size: 16px;
    }
  }
}
.word-wrapper{
  height: 35vh;
  h2{
    margin: 0;
    margin-bottom: 20px;
    font-size: 27px;
  }
  .word-text{
    font-size: 10px;
    margin-bottom: 0;
  }
}
}
</style>
