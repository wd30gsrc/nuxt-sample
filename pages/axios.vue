<template>
  <div style="text-align: center;">
    <p>{{ ip }}</p>
    <button @click="getIp">
      IPアドレスを取得
    </button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      ip: '0.0.0.0'
    }
  },
  methods: {
    async getIp () {
      this.ip = await this.$axios.$get('//icanhazip.com')
    }
  },
  head () {
    return {
      title: 'Axios'
    }
  }
}
</script>
