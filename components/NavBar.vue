<template>
  <div class="top-8 h-16 w-full absolute">
    <nav id="NavItems">
      <ul class="flex justify-center">
        <li
          v-for="item in navItems"
          :key="item.name"
          class="text-lg font-medium px-4"
        >
          <nuxt-link :to="item.link">{{ item.name }}</nuxt-link>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      navItems: [
        { name: 'About Us', link: '/' },
        { name: 'What We Do', link: '/' },
        { name: 'Our Work', link: '/' },
        { name: 'Blog', link: '/' },
        { name: 'Say Hi', link: '/' },
      ],
    }
  },
}
</script>

<style scoped>
li {
  color: #0a142f;
  line-height: 22px;
}
</style>
