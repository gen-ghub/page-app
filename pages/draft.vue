<template>
  <main v-if="data" class="main">
    <h1 class="title">{{ data.title }}</h1>
    <p class="publishedAt">{{ data.publishedAt }}</p>
    <div class="post" v-html="data.body"></div>
  </main>
</template>

<script>
import axios from 'axios'

export default {
  data() {
    return {
      data: {}
    };
  },
  async created() {
    const query = this.$route.query;
    if (query.id === undefined || query.draftKey === undefined) {
      return;
    }
    const { data } = await axios.get(
      `https://happy-shaw.microcms.io/api/v1/blog/${query.id}?draftKey=${query.draftKey}`,
      {
        headers: { 'X-API-KEY': '190b409a-566e-4d65-9583-e4876da6e482' }
      }
    )
    this.data = data;
  },
}
</script>
