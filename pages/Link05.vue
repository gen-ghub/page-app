<template>
  <div>
    <Header />
    <section class="blog-title">
      <h1>BLOG</h1>
    </section>
  <ul>
    <li v-for="content in contents" :key="content.id">
      <nuxt-link :to="`/${content.id}`">
        {{ content.title }}
        <img :src="content.image.url" alt="">
      </nuxt-link>
    </li>
  </ul>
  </div>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData({$config}) {
    const { data } = await axios.get(
      'https://happy-shaw.microcms.io/api/v1/blog',
      {
        headers: { 'X-API-KEY': '190b409a-566e-4d65-9583-e4876da6e482' }
      }
    )
    return data
  }
}
</script>

<style lang="scss" scoped>
  .blog-title{
    height: 30vh;
    width: 100vw;
    background-color: rgba( #b9b9b9ad,  0.2);
    display: flex;
    align-items: center;
    h1{
      margin-left: 15vw;
      font-size: 1.5vw;
      font-weight: 300;
      letter-spacing: 4px;
    }
  }
</style>
