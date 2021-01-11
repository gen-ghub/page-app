<template>
<div>
  <Header />
  <div class="relative">
    <img class="contact-img" src="~/assets/sun.jpg" />
    <h2 class="contact-title absolute text-white font-serif">Be free within constraints</h2>
    <h4 class="contact-sab-title absolute text-white font-serif">CONTACT</h4>
  </div>
  <section class="contact-container border-b-2">
    <div class="flex justify-center">
      <template v-if="!finished">
        <form class="mb-20" name="contact" method="POST" data-netlify="true" @submit.prevent>
          <h4 class="font-serif">Question and Offer</h4>
          <p class="flex flex-col mb-2">
            <input
              class="pl-2 border border-gray-400 mb-2"
              v-model="form.name"
              type="text"
              name="name"
              placeholder="Name"
            />
            <input
              class="pl-2 border border-gray-400 mb-2"
              v-model="form.email"
              type="email"
              name="email"
              placeholder="Email"
            />
            <textarea
              class="text-sm pl-2 border border-gray-400 h-40"
              id="form-content"
              v-model="form.content"
              name="content"
              placeholder="Write a message..."
            />
          </p>
          <div class="" v-show="false">
            <label for="message">スパムでない場合は空欄</label>
            <input type="text" name="bot-field" v-model="botField" />
          </div>
          <p class="flex flex-col text-xl">
            <button
              class="contact-btn text-white rounded border border-gray-400 border-opacity-75 py-2 bg-gray-700 hover:bg-gray-900 "
              @click="handleSubmit"
              v-text="'SEND'"
            />
          </p>
        </form>
      </template>
      <template v-else>
        <div class="text-4xl p-20">
          <p v-text="'お問い合わせ頂きありがとうございました。'" />
          <div class="flex justify-center">
            <nuxt-link
              class="rounded mt-20 py-2 px-20 hover:bg-blue-900"
              to="/"
              v-text="'TOPへ'"
            />
          </div>
        </div>
      </template>
    </div>
  </section>
</div>
</template>
<script>
import axios from 'axios'
export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        content: '',
      },
      finished: false,
    }
  },
  methods: {
    encode(data) {
      return Object.keys(data)
        .map(
          (key) => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
        )
        .join('&')
    },
    handleSubmit() {
      const axiosConfig = {
        header: { 'Content-Type': 'application/x-www-form-urlencoded' },
      }
      axios
        .post(
          '/',
          this.encode({
            'form-name': 'contact',
            ...this.form,
          }),
          axiosConfig
        )
        .then(() => {
          this.finished = true
        })
    },
  },
}
</script>
<style lang="scss" scoped>
.contact-container {
  padding-top: 10vh;
}
p {
  padding: 10px;
}
.contact-img{
  height: 56vh;
  width: 100vw;
  object-fit: cover;
}
.contact-title{
  top: 20vh;
  left: 35vw;
  font-size:2.5vw;
  font-weight: 100;
}
.contact-sab-title{
  top: 30vh;
  left: 45vw;
  font-size: 25px;
}
input{
  width: 30vw;
}

.contact-btn{
  width: 15vw;
}
</style>
