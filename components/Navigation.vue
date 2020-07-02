<template>
  <div>
    <ul class="local-nav">
      <li class="local-nav__item">
        <nuxt-link to="/">
          Top
        </nuxt-link>
      </li>
      <li class="local-nav__item">
        <nuxt-link to="/about">
          About
        </nuxt-link>
      </li>
      <li class="local-nav__item">
        <nuxt-link to="/blog">
          Blog
        </nuxt-link>
      </li>
      <li class="local-nav__item">
        <nuxt-link to="/blog/99">
          Blog99
        </nuxt-link>
      </li>
      <li class="local-nav__item">
        <nuxt-link to="/element">
          Element
        </nuxt-link>
      </li>
      <li class="local-nav__item">
        <nuxt-link to="/axios">
          Axios
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.local-nav {
  list-style: none;
  font-weight: bold;
  display: flex;
  flex-wrap: wrap;
  &__item {
    padding: 0 10px 0;
  }
  a {
    text-decoration: none;
    color: #333;
    line-height: 30px;
  }
}
</style>
