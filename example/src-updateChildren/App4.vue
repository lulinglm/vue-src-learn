<!-- 元素反转 + 新增元素 -->
<template>
  <div id="app">
    <div>
      <ul>
        <li v-for="item in items" :key="item.id">{{ item.val }}</li>
      </ul>
    </div>
    <button @click="change">change</button>
  </div>
</template>

<script>
export default {
  name: "App4",
  data() {
    return {
      items: [
          {id: 1, val: 'A'},
          {id: 2, val: 'B'},
          {id: 3, val: 'C'},
          {id: 4, val: 'D'}
        ]
    };
  },
  methods: {
    change() {
      this.items.reverse().push({id: 4, val: 'E'})
    }
  }
};
</script>