<template>
  <div>
    <Header />
    <div class="detalis-wrapper">
      <div class="topics-title flex justify-center ">
        <h1 class="tracking-widest">Topics</h1>
      </div>
      <div class="flex justify-center">
        <section class="main shadow-2xl">
          <p class="day">{{ today }}</p>
          <h1 class="title font-bold">{{ title }}</h1>
          <img :src="image.url" alt="">
          <div class="post" v-html="text"></div>
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData({ params }) {
    const { data } = await axios.get(
      `https://happy-shaw.microcms.io/api/v1/news/${params.slug}`,
      {
        headers: { 'X-API-KEY': '190b409a-566e-4d65-9583-e4876da6e482' }
      }
    )
    return data
  }
}
</script>

<style lang="scss" scoped>
.detalis-wrapper{
  background-color: rgba(#b9b9b9ad, 0.2);
  .topics-title{
    height: 25vh;
    align-items: center;
    font-size: 50px;
  }
}
.main {
  padding: 40px;
  margin-bottom: 5vh;
  width: 55vw;
  background-color: #fff;
  border-top: 8px solid rgb(209, 136, 0);
  .day{
    margin-bottom: 4px;
  }
  .title {
    margin-bottom: 20px;
    font-size: 20px;
  }
  img{
    height: 300px;
    width: 300px;
    object-fit: cover;
    margin-bottom: 50px;
  }
}




</style>
