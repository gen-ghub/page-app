<template>
  <div>
    <Header />
    <section class="news-title">
      <h1>NEWS</h1>
    </section>
    <section>
      <ul class="flex flex-wrap justify-center my-24">
        <li class="news-content-li" v-for="content in contents" :key="content.id">
          <nuxt-link :to="`/${content.id}/news`">
            <img class="news-content-image" :src="content.image.url" alt="" />
            <p class="news-content-day font-thin text-sm tracking-wider">{{ content.today}}</p>
            <h1 class="news-content-title tracking-widest">{{ content.title }}</h1>
            <p class="news-content-text font-extralight">{{ content.text }}</p>
          </nuxt-link>
        </li>
      </ul>
    </section>
  </div>
</template>

<script>
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
}
</script>

<style lang="scss" scoped>
.news-title {
  height: 30vh;
  width: 100vw;
  background-color: rgba(#b9b9b9ad, 0.2);
  display: flex;
  align-items: center;
  h1 {
    margin-left: 15vw;
    font-size: 1.5vw;
    font-weight: 300;
    letter-spacing: 5px;
  }
}
.news-content-li{
  padding: 10px ;
  margin-bottom: 50px;
}
.news-content-image{
  height: 400px;
  width: 400px;
  object-fit: cover;
}
.news-content-day{
  margin-top: 20px;
  margin-bottom: 8px;
}
.news-content-title{
  font-size: 20px;
  margin-bottom: 10px;
}
.news-content-text{
  width: 400px;
}
</style>
