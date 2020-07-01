<template>
  <div>
    <ul class="local-nav">
      <li>
        <nuxt-link to="/">
          Top
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">
          About
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/blog">
          Blog
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/blog/99">
          Blog99
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/element">
          Element
        </nuxt-link>
      </li>
      <li>
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
  a {
    text-decoration: none;
    color: #333;
    line-height: 30px;
  }
}
</style>
