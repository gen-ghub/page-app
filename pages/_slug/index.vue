<template>
  <div>
    <Header />
    <div class="detalis-wrapper">
      <div class="topics-title">
        <h1>Topics</h1>
      </div>
      <main class="main">
        <h1 class="title">{{ title }}</h1>
        <p class="day">{{ day }}</p>
        <p class="category">{{ category && category.name }}</p>
        <img :src="image.url" alt="">
        <div class="post" v-html="content"></div>
      </main>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  async asyncData({ params }) {
    const { data } = await axios.get(
      `https://happy-shaw.microcms.io/api/v1/blog/${params.slug}`,
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
}
.main {
  width: 960px;
  margin: 0 auto;
}

.title {
  margin-bottom: 20px;
}

.publishedAt {
  margin-bottom: 40px;
}

.post {
  & > h1 {
    font-size: 30px;
    font-weight: bold;
    margin: 40px 0 20px;
    background-color: #eee;
    padding: 10px 20px;
    border-radius: 5px;
  }

  & > h2 {
    font-size: 24px;
    font-weight: bold;
    margin: 40px 0 16px;
    border-bottom: 1px solid #ddd;
  }

  & > p {
    line-height: 1.8;
    letter-spacing: 0.2px;
  }

  & > ol {
    list-style-type: decimal;
    list-style-position: inside;
  }
}
</style>
