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
  padding: 40px 40px 15vh 40px;
  margin-bottom: 10vh;
  width: 55vw;
  background-color: #fff;
  border-top: 8px solid #F5DF4D;
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
@media screen and (max-width: 1440px){
  .main {
  width: 60vw;
}
}
@media screen and (max-width: 1024px){
  .main {
  width: 70vw;
}
}
@media screen and (max-width: 425px){
  .detalis-wrapper{
  .topics-title{
    height: 20vh;
    font-size: 40px;
  }
}
.main {
  padding: 30px 30px 10vh 30px;
  width: 75vw;
  .day{
    font-size: 12px;
  }
  .title {
    font-size: 20px;
  }
  img{
    height: 250px;
    width: 250px;
    margin-bottom: 40px;
  }
  .post{
    font-size: 14px;
  }
}
}
@media screen and (max-width: 375px){
  .detalis-wrapper{
  .topics-title{
    height: 15vh;
    font-size: 30px;
  }
}
  .main {
  width: 78vw;
  .day{
    font-size: 10px;
  }
  .title {
    font-size: 18px;
  }
  img{
    height: 200px;
    width: 200px;
  }
}
}
</style>
