# Switch 开关

开关按钮，用于表示开关状态/两种状态之间的切换

### 使用

```vue
<template>
  <div>
    <div class="title">基础用法</div>
    <top-switch v-model="value1" @click="changeBtn1"></top-switch>
    <div class="title">禁用</div>
    <top-switch v-model="value2" :disabled="true"></top-switch>
    <div class="title">自定义颜色</div>
    <top-switch
      v-model="value3"
      @click="changeBtn3"
      active-color="#ff414d"
      in-active-color="#ffdd94"
    ></top-switch>
  </div>
</template>

<script>
export default {
  data() {
    return {
      value1: false,
      value2: false,
      value3: false,
    }
  },
  methods: {
    changeBtn1() {
      this.value1 = !this.value1
    },
    changeBtn3() {
      this.value3 = !this.value3
    },
  },
}
</script>
```

### 属性

| 属性            | 说明           | 类型    | 默认值  | 可选值       |
| :-------------- | :------------- | :------ | :------ | :----------- |
| v-model         | 开关状态       | Boolean | false   | true / false |
| disabled        | 是否禁用       | Boolean | false   | true / false |
| active-color    | 激活状态颜色   | String  | #fa897b | -            |
| in-active-color | 未激活状态颜色 | String  | #b6b6b6 | -            |

<style>
table th:first-of-type {
  width: 20%;
}
table th:nth-of-type(2) {
  width: 25%;
}
table th:nth-of-type(3) {
  width: 20%;
}
table th:nth-of-type(4) {
  width: 15%;
}
table th:nth-of-type(5) {
  width: 20%;
}
</style>
