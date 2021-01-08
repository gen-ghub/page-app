<template>
  <ul>
    <li v-for="content in contents" :key="content.id">
      <nuxt-link :to="`/${content.id}`">
        {{ content.title }}
      </nuxt-link>
    </li>
  </ul>
</template>

<script>
import axios from 'axios'
export default {
  async asyncData() {
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
