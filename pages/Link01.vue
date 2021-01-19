<template>
  <div>
    <Header />
    <section class="news-title">
      <h1>NEWS</h1>
    </section>
    <section class="main flex justify-center ">
      <ul class="news-wrapper flex flex-wrap content-center ">
        <li class="news-content-li " v-for="content in contents" :key="content.id">
          <nuxt-link :to="`/${content.id}/news`">
            <img class="news-content-image" :src="content.image.url" alt="" />
            <p class="news-content-day font-thin text-sm tracking-wider">{{ content.today}}</p>
            <h1 class="news-content-title tracking-widest">{{ content.title }}</h1>
            <!-- <p class="news-content-text font-extralight">{{ content.text }}</p> -->
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

.main{
  margin: 10vh 10vw;
  .news-wrapper{
    padding-left: 2.5vw;
  }
}

.news-title {
  height: 30vh;
  width: 100vw;
  background-color: rgba(#b9b9b9ad, 0.2);
  display: flex;
  align-items: center;
  h1 {
    margin-left: 15vw;
    font-size: 25px;
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
@media screen and (max-width: 1440px){
.main{
  margin: 10vh 5vw;
  .news-wrapper{
    padding-left: 20px;
  }
}
}
@media screen and (max-width: 1024px){
.main{
  margin: 10vh 5vw;
  .news-wrapper{
    padding-left: 4vw;
  }
}
}
@media screen and (max-width: 768px){
.main{
  margin: 10vh 10vw;
  .news-wrapper{
    padding-left: 13vw;
  }
}
}
@media screen and (max-width: 425px){
.main{
  margin: 8vh 10vw;
  .news-wrapper{
    padding-left: 8vw;
  }
}
.news-title {
  height: 20vh;
  h1 {
    font-size: 20px;
  }
}
.news-content-image{
  height: 250px;
  width: 250px;
}
.news-content-text{
  width: 250px;
}
}
@media screen and (max-width: 375px){
  .main{
  margin: 8vh 10vw;
  .news-wrapper{
    padding-left: 8vw;
  }
}
  .news-content-image{
  height: 200px;
  width: 200px;
}
.news-content-text{
  width: 200px;
  font-size: 12px;
}
.news-content-title{
  font-size: 16px;
  margin-bottom: 6px;
}
.news-content-day{
  margin-top: 5px;
  margin-bottom:5px;
  font-size: 12px;
}
}
@media screen and (max-width: 320px){
  .main{
  margin: 8vh 10vw;
  .news-wrapper{
    padding-left: 5vw;
  }
}
  .news-content-image{
  height: 200px;
  width: 200px;
}
.news-content-text{
  width: 200px;
  font-size: 12px;
}
.news-content-title{
  font-size: 16px;
  margin-bottom: 6px;
}
.news-content-day{
  margin-top: 5px;
  margin-bottom:5px;
  font-size: 12px;
}
}
</style>

