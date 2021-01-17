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
        <validation-observer class="mb-20" ref="observer" v-slot="{ invalid, validated }" tag="form" name="contact" method="POST" data-netlify="true" netlify-honeypot="bot-field" @submit.prevent>
          <h4 class="font-serif">Question and Offer</h4>
          <p class="flex flex-col mb-2">
            <validation-provider v-slot="{ errors }" rules="required|max:100" name="お名前">
                <input class="contact-input pl-2 border border-gray-400 mb-2" type="text" id="username" name="username" v-model="username" autocomplete="name" placeholder="Name">
                <p v-show="errors.length" class="p-contact_error ">{{ errors[0] }}</p>
              </validation-provider>
            <validation-provider v-slot="{ errors }" rules="required|email|max:256" name="メールアドレス">
                <input class="contact-input pl-2 border border-gray-400 mb-2" type="text" id="useremail" name="useremail" v-model="useremail" autocomplete="email" placeholder="Email">
                <p v-show="errors.length" class="p-contact_error ">{{ errors[0] }}</p>
              </validation-provider>
            <validation-provider v-slot="{ errors }" rules="required|max:1000" name="お問い合わせ内容">
                <textarea class="contact-textarea text-sm pl-2 border border-gray-400" id="message" name="message" v-model="message" placeholder="Write a message..."></textarea>
                <p v-show="errors.length" class="p-contact_error ">{{ errors[0] }}</p>
              </validation-provider>
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
        </validation-observer>
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
  font-size:40px;
  font-weight: 100;
}
.contact-sab-title{
  top: 30vh;
  left: 45vw;
  font-size: 25px;
}
.contact-input{
  width: 400px;
}
.contact-textarea{
  width: 600px;
  height: 30vh;
}
.p-contact_error{
  font-size: 16px;
}
.contact-btn{
  width: 15vw;
}
@media screen and (max-width: 1024px){
  .contact-title{
  left: 29vw;
  font-size:35px;
}
.contact-sab-title{
  left: 43vw;
  font-size: 22px;
}
}
@media screen and (max-width: 768px){
  .contact-title{
  left: 23vw;
  font-size:35px;
}
.contact-sab-title{
  left: 41vw;
  font-size: 22px;
}
}
@media screen and (max-width: 767px){
  .contact-input{
  width: 300px;
}
.contact-textarea{
  width: 400px;
  height: 30vh;
}
.contact-btn{
  width: 100px;
}
}
@media screen and (max-width: 425px){
  .contact-img{
  height: 40vh;
}
  .contact-title{
  top: 13vh;
  left: 22vw;
  font-size:20px;
}
.contact-sab-title{
  top: 20vh;
  left: 41vw;
  font-size: 16px;
}
  .contact-input{
  width: 250px;
}
.contact-textarea{
  width: 300px;
}
}
@media screen and (max-width: 320px){
  .contact-input{
  width: 200px;
}
.contact-textarea{
  width: 250px;
}
}
</style>
