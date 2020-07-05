<template>
  <div>
    <my-calender class="panel-default">
      <template v-slot:slot-header>
        <h1>Here mtght be a page title</h1>
      </template>
      <!-- <p slot-scope="propsdata">
        スロットから受け取ったtext => {{ propsdata.text }}
      </p> -->
      <template v-slot:default="slotProps">
        {{ slotProps.user[0].firstName }}
      </template>
      <template v-slot:slot-footer>
        <p>Here's some contact info</p>
      </template>
    </my-calender>
  </div>
</template>

<script>
import MyCalender from '~/components/MyCalender.vue'

export default {
  components: {
    MyCalender
  }
}
</script>
