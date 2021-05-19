# Toast 轻提示

弹出式消息提示

### 使用

```vue
<template>
  <div>
    <top-toast :visible="showPrimary" type="primary">这是一段通知</top-toast>
    <div class="title">基础用法</div>
    <div class="btns">
      <top-button type="primary" @click="primary">文字提示</top-button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showPrimary: false,
    }
  },
  methods: {
    primary() {
      this.showPrimary = true
      setTimeout(() => {
        this.showPrimary = false
      }, 2000)
    },
  },
}
</script>
```

### 属性

| 属性    | 说明       | 类型    | 默认值  | 可选值                                      |
| :------ | :--------- | :------ | :------ | :------------------------------------------ |
| visible | 显示与隐藏 | Boolean | false   | true / false                                |
| type    | 类型       | String  | primary | primary / success / warning / danger / info |

<style>
table th:first-of-type {
  width: 10%;
}
table th:nth-of-type(2) {
  width: 20%;
}
table th:nth-of-type(3) {
  width: 15%;
}
table th:nth-of-type(4) {
  width: 15%;
}
table th:nth-of-type(5) {
  width: 40%;
}
</style>
