<template>
  <div>
    <response-component value="componentsA" :title="returnTitle" />
    <response-component id="parent" value="componentsB" class="parent" />
  </div>
</template>

<script>
import ResponseComponent from '~/components/ResponseComponent.vue'
export default {
  components: {
    ResponseComponent
  },
  data () {
    return {
      returnTitle: 'return title'
    }
  }
}
</script>
