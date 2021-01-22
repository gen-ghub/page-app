<template>
  <section>
    <TopImage />
    <section>
      <div class="top-news bg-gray-100 flex justify-center items-center">
        <h1 class="text-2xl font-light tracking-widest">NEWS</h1>
      </div>
      <section class=" w-screen grid grid-cols-8 gap-6 py-20">
        <div class="col-start-2 col-span-6 ">
          <div class="flex justify-center items-center space-x-6">
            <ul >
              <li class="mb-4"><img class="" :src="contents[0].image.url" alt="" /></li>
              <li class="mb-1"><p class="text-xs">{{ contents[0].today }}</p></li>
              <li class="mb-2"><p class="text-xl">{{ contents[0].title }}</p></li>
              <li class="mb-4"><p class="news-text font-thin leading-relaxed">{{ contents[0].text | ellipsis}}</p></li>
              <li><nuxt-link :to="`/${contents[0].id}/news`" class="read p-2 rounded text-yellow-500 hover:bg-gray-100  transition duration-700">READ MORE</nuxt-link></li>
            </ul>
            <ul>
              <li class="mb-4"><img class="" :src="contents[3].image.url" alt="" /></li>
              <li class="mb-1"><p class="text-xs">{{ contents[3].today }}</p></li>
              <li class="mb-2"><p class="text-xl">{{ contents[3].title }}</p></li>
              <li class="mb-4"><p class="news-text font-thin leading-relaxed">{{ contents[3].text | ellipsis}}</p></li>
              <li><nuxt-link :to="`/${contents[0].id}/news`" class="read p-2 rounded text-yellow-500 hover:bg-gray-100  transition duration-700">READ MORE</nuxt-link></li>
            </ul>
            <ul>
              <li class="mb-4"><img class="" :src="contents[1].image.url" alt="" /></li>
              <li class="mb-1"><p class="text-xs">{{ contents[1].today }}</p></li>
              <li class="mb-2"><p class="text-xl">{{ contents[1].title }}</p></li>
              <li class="mb-4"><p class="news-text font-thin leading-relaxed">{{ contents[1].text | ellipsis}}</p></li>
              <li><nuxt-link :to="`/${contents[1].id}/news`" class="read p-2 rounded text-yellow-500 hover:bg-gray-100  transition duration-700">READ MORE</nuxt-link></li>
            </ul>
          </div>
        </div>
      </section>
          <div class="flex justify-center items-center mb-20">
            <nuxt-link class="col-start-5 col-span-1 px-8 py-2 text-black rounded border border-gray-400 border-opacity-75 bg-gray-200 hover:bg-gray-900 hover:text-white transition duration-700" to="/Link01">read more</nuxt-link>
          </div>
    </section>
    <Work />
  </section>
</template>

<script>
import TopImage from '@/components/TopImage.vue'
import Work from '@/components/Work.vue'
import axios from 'axios'

export default {
  async asyncData({ $config }) {
    const { data } = await axios.get(
      'https://happy-shaw.microcms.io/api/v1/news',
      {
        headers: { 'X-API-KEY': '190b409a-566e-4d65-9583-e4876da6e482' },
      }
    )
    return data
  },
  components: {
    TopImage,
    Work
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }
      ]
    }
  },
  name: "demo",
        filters:{
            ellipsis(value){
                if (!value) return '';
                if (value.length > 50) {
                    return value.slice(0,50) + '...'
                }
                return value
            }
        }
}
</script>

<style lang="scss" scoped>
.read{
  text-decoration: underline;

}
.top-news{
  height: 18vh;
}
.news-text{
  width: 400px;
  height: 100px;
}
img{
  height: 400px;
  width: 400px;
  object-fit: cover;
}
@media screen and (max-width: 1024px){
  .w-screen{
    display: none;
  }
}
  @media screen and (max-width: 425px){

  }
    @media screen and (max-width: 375px){
  }
    @media screen and (max-width: 320px){

  }
</style>
