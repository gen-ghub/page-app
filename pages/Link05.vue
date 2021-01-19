<template>
  <div>
    <Header />
    <section class="blog-title">
      <h1>BLOG</h1>
    </section>
    <ul class="blog-wrapper flex flex-wrap justify-center">
      <li class="blog-content-li" v-for="content in contents" :key="content.id">
        <nuxt-link :to="`/${content.id}`">
          <img class="blog-content-image" :src="content.image.url" alt="" />
          <p class="blog-content-day font-thin text-sm tracking-wider">
            {{ content.day }}
          </p>
          <h1 class="blog-content-title tracking-widest">
            {{ content.title }}
          </h1>
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData({ $config }) {
    const { data } = await axios.get(
      'https://happy-shaw.microcms.io/api/v1/blog',
      {
        headers: { 'X-API-KEY': '190b409a-566e-4d65-9583-e4876da6e482' },
      }
    )
    return data
  },
}
</script>

<style lang="scss" scoped>
@media screen and (min-width: 1640px){
  .blog-wrapper{
    margin: 10vh 10vw;
  }
}

.blog-title {
  height: 30vh;
  width: 100vw;
  background-color: rgba(#b9b9b9ad, 0.2);
  display: flex;
  align-items: center;
  h1 {
    margin-left: 15vw;
    font-size: 25px;
    font-weight: 300;
    letter-spacing: 4px;
  }
}
.blog-content-li {
  padding: 10px;
  margin-bottom: 50px;
}
.blog-content-image {
  height: 400px;
  width: 400px;
  object-fit: cover;
}
.blog-content-day {
  margin-top: 20px;
  margin-bottom: 8px;
}
.blog-content-title {
  font-size: 20px;
  margin-bottom: 10px;
}
</style>
