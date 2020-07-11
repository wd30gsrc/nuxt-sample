<template>
  <div>
    <p>{{ host }}</p>
    <button @click="sendRequest">
      リクエスト
    </button>
    <p>{{ accept }}</p>
  </div>
</template>

<script>
export default {
  async asyncData ({ app }) {
    const response = await app.$axios.$get('https://httpbin.org/get')
    return { host: response.headers.Host }
  },
  data () {
    return {
      host: '',
      accept: ''
    }
  },
  methods: {
    async sendRequest () {
      const response = await this.$axios.$get('https://httpbin.org/get')
      this.accept = response.headers.Accept
    }
  }
}
</script>
