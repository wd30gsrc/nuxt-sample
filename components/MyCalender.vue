<template>
  <div class="panel">
    <header>
      <slot name="slot-header" />
    </header>
    <main>
      <!-- <slot text="Hello!"></slot> -->
      <slot :user="user">
        {{ user[1].lastName }}
      </slot>
    </main>
    <footer>
      <slot name="slot-footer" />
    </footer>
  </div>
</template>

<script>
export default {
  props: {
    header: {
      type: String,
      default: 'return header'
    }
    // text: {
    //   type: String,
    //   default: 'default props text'
    // }
  },
  data () {
    return {
      user: [
        { firstName: 'taro', lastName: 'yamada' },
        { firstName: 'taro2', lastName: 'yamada2' }
      ],
      testdata: 'testData'
    }
  }
}
</script>

<style>

</style>
