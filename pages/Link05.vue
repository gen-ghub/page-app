<template>
  <div>
    <Header />
    <section class="blog-title">
      <h1>BLOG</h1>
    </section>
    <section class="main flex justify-center">
      <ul class="blog-wrapper flex flex-wrap content-center">
        <li class="blog-content-li shadow-2xl" v-for="content in contents" :key="content.id">
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
    </section>
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
.main {
  margin: 10vh 8vw;
  .blog-wrapper {
    padding-left: 2.5vw;
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
    letter-spacing: 5px;
  }
}
.blog-content-li {
  padding: 20px;
  margin: 0 10px 50px 10px;
  border-top: 8px solid #F5DF4D;
}
.blog-content-image {
  height: 380px;
  width: 380px;
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
@media screen and (max-width: 1440px) {
  .main {
    margin: 10vh 3vw;
    .blog-wrapper {
      padding-left: 20px;
    }
  }
}
@media screen and (max-width: 1024px) {
  .main {
    margin: 10vh 3vw;
    .blog-wrapper {
      padding-left: 4vw;
    }
  }
}
@media screen and (max-width: 768px) {
  .main {
    margin: 10vh 8vw;
    .blog-wrapper {
      padding-left: 13vw;
    }
  }
}
@media screen and (max-width: 425px) {
  .main {
    margin: 8vh 6vw;
    .blog-wrapper {
      padding-left: 8vw;
    }
  }
  .blog-title {
    height: 20vh;
    h1 {
      font-size: 20px;
    }
  }
  .blog-content-image {
    height: 250px;
    width: 250px;
  }
  .blog-content-text {
    width: 250px;
  }
}
@media screen and (max-width: 375px) {
  .main {
    margin: 8vh 7vw;
    .blog-wrapper {
      padding-left: 8vw;
    }
  }
  .blog-content-image {
    height: 200px;
    width: 200px;
  }
  .blog-content-text {
    width: 200px;
    font-size: 12px;
  }
  .blog-content-title {
    font-size: 16px;
    margin-bottom: 6px;
  }
  .blog-content-day {
    margin-top: 5px;
    margin-bottom: 5px;
    font-size: 12px;
  }
}
@media screen and (max-width: 320px) {
  .main {
    margin: 8vh 6vw;
    .blog-wrapper {
      padding-left: 4vw;
    }
  }
  .blog-content-image {
    height: 200px;
    width: 200px;
  }
  .blog-content-text {
    width: 200px;
    font-size: 12px;
  }
  .blog-content-title {
    font-size: 16px;
    margin-bottom: 6px;
  }
  .blog-content-day {
    margin-top: 5px;
    margin-bottom: 5px;
    font-size: 12px;
  }
}
</style>
