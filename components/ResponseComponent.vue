<template>
  <div id="child" class="child">
    <p>{{ value }}: {{ title }}</p>
    <div>
      <ul>
        <li v-for="item in items" :key="item.id">
          name:{{ item.name }}, hp: {{ item.hp }}
          <br>
          <button @click="doAttack">
            attack
          </button>
        </li>
      </ul>
    </div>
    <div>
      <p>increment function</p>
      <div>{{ increment_num }}</div>
      <button @click="increment">
        +1
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: String,
      default: 'Default value'
    },
    title: {
      type: String,
      default: 'Default title'
    }
  },
  data () {
    return {
      items: [
        { id: 1, name: 'slime', hp: '100' },
        { id: 2, name: 'goblin', hp: '200' },
        { id: 3, name: 'dragon', hp: '300' }
      ],
      increment_num: 0
    }
  },
  methods: {
    doAttack () {
      const item = this.items.forEach((el) => {
        el.hp -= 10
      })
      return item
    },
    increment () {
      this.increment_num += 1
    }
  }
}
</script>

<style scoped>
.child {
  padding: 20px;
}
</style>
