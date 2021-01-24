<template>
  <div>
    <div class="grid grid-cols-2 h-full">
      <section
        class="col-span-2 lg:col-span-1 lg:col-start-1 bg-gray-200 flex justify-center"
      >
        <div class="flex flex-col items-center enterme-wrapper">
          <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-4">
            Entertainment Agent
          </h2>
          <h1 class="tracking-widest text-xl font-extralight mb-10">
            エンターテインメント・エージェント
          </h1>
          <div
            class="leading-loose text-sm flex flex-col items-center font-thin tracking-widest mb-16 enterme-text"
          >
            <p class="mb-8">エンターテインメントで『世界をつなぐ』</p>
            <p>タレントブッキング</p>
            <p>広告キャスティング</p>
            <p>イベント／ライブ制作</p>
            <p>ファンクラブ運営／ライセンス</p>
            <p>グッズ製作／ECサイト運営</p>
            <p class="mb-8">コンサルティング</p>
            <p>
              Taylor Swift、Katy Perry、Backstreet Boys、KISSといった<br />世界的アーティストの日本における活動を幅広くサポート。
            </p>
            <p>
              海外のタレント起用、イベント出演ブッキング、コラボレーション企画、ライセンス等ご相談に乗ります。
            </p>
          </div>
          <nuxt-link to="/Contact" class="mb-32 contact-btn">
            <button
              class="w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black hover:bg-gray-900 hover:text-white transition duration-700"
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
      <section
        class="col-span-2 lg:col-span-1 lg:col-start-2 bg-gray-200 flex justify-center items-center"
      >
        <div class="flex flex-col items-center trans-wrapper">
          <h2 class="text-yellow-600 text-5xl font-thin mt-24 mb-4">
            Creative Translator
          </h2>
          <h1 class="tracking-widest text-xl font-extralight mb-10">
            クリエイティブ翻訳家
          </h1>
          <div
            class="leading-loose text-sm flex flex-col items-center font-thin tracking-widest mb-16 trans-text"
          >
            <p class="mb-8">『世界に伝えたい』を叶える</p>
            <p class="mb-8">
              クリエイティブ翻訳でお客さまが世界にファンを作るお手伝いをします
            </p>
            <p class="mb-8 p-wied">
              翻訳と似ているようで違う「LOCALIZATION」は、日本語で「地域化」という意味で、国によって異なる文化や習慣、流行、価値観といったさまざまな背景を考慮した上で、ある国を対象に作られたサービスや文面を、他の国での展開に対応させること。
            </p>
            <p class="mb-8 p-wied">
              また、トランスレーション（翻訳）とクリエイション（創造）を組み合わせた「TRANSCREATION」は、広告や芸術的作品のメッセージ性、スタイル、トーンを維持しながら、ブランディングやターゲットに合わせて、ある言語から他の言語に対応させること。
            </p>
            <p class="mb-8 p-wied">
              バイリンガルならではの翻訳技術で、ブランドやアーティストのサイト・SNS・カタログといったクリエイティブを、単なる翻訳ではなく、響きが良く、訴求力のあるコピーやテキストになるよう、原文やイメージに合わせて翻訳いたします。
            </p>
            <p>対応言語：日本語⇔英語</p>
          </div>
          <nuxt-link to="/Contact" class="mb-32 contact-btn">
            <button
              class="w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black hover:bg-gray-900 hover:text-white transition duration-700"
            >
              Contact
            </button>
          </nuxt-link>
        </div>
      </section>
      <div class="col-span-2 lg:col-start-1 lg:hidden bg-green-200">
        <img class="h-full w-full object-cover" src="~/assets/sun.jpg" />
      </div>
      <section
        class="col-span-2 lg:col-span-1 lg:col-start-1 bg-gray-200 flex justify-center items-center profile-wrapper"
      >
        <div class="flex flex-col items-center profile-main">
          <h1 class="text-3xl tracking-widest font-semibold">Rika Miyashita</h1>
          <h2 class="mb-20">みやしたりか</h2>
          <div class="">
            <p class="m-auto pb-8 p-wied leading-relaxed">
              日本で生まれ、幼少期より在米。日本語／英語のバイリンガル
              慶應義塾大学から米テキサスの大学に編入・卒業。舞台芸術を専攻。
              帰国後、舞台監督志望として劇団に所属。コンサートプロモーターに転属しイベント制作に従事した後、海外のアーティストやブランドを専門としたエージェンシーに勤務。イベント、ファンクラブ、広告キャスティング、撮影コーディネート等の分野で活動。
              ココナラ翻訳部門1位獲得、販売実績500件以上、満足度5.0/5.0。音楽・アート・ファッション・旅行の分野で実績多数。
            </p>
            <div class="flex justify-center">
              <nuxt-link to="/Link04">
                <button
                  class="tracking-widest text-lg w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black hover:bg-gray-900 hover:text-white transition duration-700"
                >
                  profile
                </button>
              </nuxt-link>
              <nuxt-link to="/Link05" class="ml-8">
                <button
                  class="tracking-widest text-lg w-32 py-2 border border-gray-400 border-opacity-50 rounded text-black hover:bg-gray-900 hover:text-white transition duration-700"
                >
                  blog
                </button>
              </nuxt-link>
            </div>
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
        <div
          class="leading-loose flex flex-col items-center font-thin tracking-widest mb-16 word-text"
        >
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
.p-wied {
  width: calc(100% - 20%);
}
h2 {
  font-family: cursive;
}
.user-img {
  height: 820px;
  width: 100%;
}
@media screen and (max-width: 1024px) {
  .user-img {
    height: 600px;
  }
  .enterme-wrapper {
    h2 {
      font-size: 40px;
      margin-top: 40px;
    }
    .enterme-text {
      margin-bottom: 30px;
    }
  }
  .trans-wrapper {
    h2 {
      font-size: 35px;
      margin-top: 40px;
    }
    .trans-text {
      margin-bottom: 30px;
    }
  }

  .contact-btn {
    margin-bottom: 40px;
  }
  .word-wrapper {
    height: 70vh;
    h2 {
      margin-top: 40px;
    }
  }
}
@media screen and (max-width: 768px) {
  .profile-wrapper {
    .profile-main {
      margin: 20vh 0;
    }
  }
}
@media screen and (max-width: 425px) {
  .user-img {
    height: 380px;
  }
  .enterme-wrapper {
    h2 {
      font-size: 30px;
      margin-top: 40px;
    }
    h1 {
      font-size: 16px;
      margin-bottom: 30px;
    }
    .enterme-text {
      margin-bottom: 30px;
      .mb-8 {
        margin-bottom: 10px;
      }
      p {
        font-size: 12px;
      }
    }
  }
  .trans-wrapper {
    h2 {
      font-size: 30px;
      margin-top: 40px;
    }
    h1 {
      font-size: 16px;
      margin-bottom: 30px;
    }
    .trans-text {
      margin-bottom: 30px;
      .mb-8 {
        margin-bottom: 10px;
      }
      p {
        font-size: 12px;
      }
    }
  }
  .profile-wrapper {
    .profile-main {
      margin: 15vh 0;
    }
  }
  .contact-btn {
    margin-bottom: 30px;
  }
  .word-wrapper {
    height: 60vh;
    h2 {
      margin-top: 40px;
      font-size: 38px;
    }
  }
}
@media screen and (max-width: 375px) {
  .enterme-wrapper {
    h2 {
      font-size: 25px;
      margin-top: 30px;
      margin-bottom: 10px;
    }
    h1 {
      font-size: 14px;
      margin-bottom: 25px;
    }
    .enterme-text {
      margin-bottom: 20px;
      p {
        font-size: 10px;
      }
    }
  }
  .trans-wrapper {
    h2 {
      font-size: 25px;
      margin-top: 30px;
    }
    h1 {
      font-size: 14px;
      margin-bottom: 25px;
    }
    .trans-text {
      margin-bottom: 20px;
      .mb-8 {
        margin-bottom: 10px;
      }
      p {
        font-size: 10px;
      }
    }
  }
  .contact-btn {
    font-size: 14px;
  }
  .profile-wrapper {
    .profile-main {
      margin: 10vh 0;
      h1 {
        font-size: 25px;
        margin-bottom: 40px;
      }
    }
  }
  .word-wrapper {
    height: 50vh;
    h2 {
      margin-top: 40px;
    }
    .word-text {
      font-size: 14px;
    }
  }
}
@media screen and (max-width: 320px) {
  .trans-wrapper {
    h2 {
      font-size: 20px;
      margin-top: 25px;
      margin-bottom: 15px;
    }
    h1 {
      font-size: 13px;
      margin-bottom: 20px;
    }
  }
  .profile-wrapper {
    .profile-main {
      h1 {
        font-size: 20px;
      }
      p {
        font-size: 16px;
      }
    }
  }
  .word-wrapper {
    height: 35vh;
    h2 {
      margin: 0;
      margin-bottom: 20px;
      font-size: 27px;
    }
    .word-text {
      font-size: 10px;
      margin-bottom: 0;
    }
  }
}
</style>
