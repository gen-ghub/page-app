<template>
    <header class="pt-4 pb-4 w-full tracking-widest  ">
      <div class="grid sm:grid-cols-2 ">
        <div class="flex justify-evenly">
          <router-link to="/">
            <h1 class="text-xl font-medium">タイトル</h1>
          </router-link>
        </div>
        <nav>
      <ul class="lg:text-xl flex justify-evenly mr-8 h-full font-thin test">
        <li>
          <nuxt-link class="tracking-widest " to="/Link01">News</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link02">Entertainment</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link03">Translation</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link04">Profile</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Link05">Blog</nuxt-link>
        </li>
        <li>
          <nuxt-link class="tracking-widest  " to="/Contact">Contact</nuxt-link>
        </li>
      </ul>
              <button
          class="mobile-menu-icon"
          onclick="document.querySelector('body').classList.toggle('open');"
          id="menu-open"
          v-on:click="flag = !flag"
        >
          <span></span>
          <span></span>
          <span></span>
        </button>
        <div id="menu-bg" :class="{ open: flag }" v-on:click="flag = !flag">
          <nav id="menu-body" :class="{ open: flag }">
            <ul>
              <li v-for="menu in menus" :key="menu.title" class="menu-list">
                <nuxt-link
                  :to="menu.href"
                  v-html="menu.title"
                  class="menu-link"
                  onclick="document.querySelector('body').classList.toggle('open');"
                ></nuxt-link>
              </li>
            </ul>
          </nav>
        </div>
    </nav>
      </div>
    </header>
</template>

<script>
export default {
  data() {
    return {
      flag: false,
      menus: [
        {  href: '/Link01', title: 'News' },
        {  href: '/Link02', title: 'Entertainment' },
        {  href: '/Link03', title: 'Translation' },
        {  href: '/Link04', title: 'Profile' },
        {  href: '/Link05', title: 'Blog' },
        {  href: '/Contact', title: 'Contact' },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
#menu-open {
  display: none;
}
#menu-open {
  position: fixed;
  top: 2vw;
  right: 5vw;
  z-index: 9999;
}

#menu-bg {
  position: fixed;
  display: none;
  top: 0;
  left: 0;
  z-index: 9998;
  width: 100%;
  height: 100%;
  background: black;
  opacity: 0.7;

  &.open {
    display: block;
  }
}
#menu-body {
  position: fixed;
  top: 100px;
  right: 0;
  z-index: 9999;
  width: 63%;
  height: 100%;
  transform: translateX(100%);
  &.open {
    transform: translateX(0%);
  }
  .menu-list {
    margin-bottom: 10px;
    .menu-link {
      font-size: 30px;
      color: #fff;
    }
  }
}
@media screen and (max-width: 1024px){
  ul{
    font-size: 16px;
    li{
      margin-left: 15px;
    }
  }
}
@media screen and (max-width: 800px) {
  .test {
    display: none;
  }
  #menu-open {
    display: inline;
  }
  .mobile-menu-icon {
    background-color: unset;
    border: none;
    outline: none !important;
    cursor: pointer;

    & > span {
      background-color: Black;
      width: 40px;
      height: 3px;
      display: block;
      margin-bottom: 9px;
      transition: transform 0.7s;

      &:last-child {
        margin-bottom: 0;
      }
    }
  }
    .open {
    background-color: Black;

    & .mobile-menu-icon {
      & > span {
        background-color: White;

        &:nth-child(1) {
          transition-delay: 70ms;
          transform: translateY(12px) rotate(135deg);
        }
        &:nth-child(2) {
          transition-delay: 0s;
          transform: translateX(-18px) scaleX(0);
        }
        &:nth-child(3) {
          transition-delay: 140ms;
          transform: translateY(-12px) rotate(-135deg);
        }
      }
    }
  }
}

@media screen and (max-width: 767px) {
  header {
    padding-top: 1.2rem;
    padding-bottom: 1rem;
  }
  header.scroll-nav {
    padding-top: 0.9rem;
    padding-bottom: 0.7rem;
  }
}
@media screen and (max-width: 425px) {
  header {
    .header-title {
      a {
        font-size: 20px;
      }
    }
  }
  header.scroll-nav {
    padding-top: 1rem;
    padding-bottom: 0.8rem;
    .header-title {
      a {
        font-size: 18px;
      }
    }
    border-bottom: 1px solid #022444;
  }
  #menu-open {
    top: 4vw;
    right: 5vw;
  }
  #menu-body {
    width: 63%;
    .menu-list {
      margin-bottom: 10px;
      .menu-link {
        font-size: 22px;
      }
    }
  }
}
</style>

