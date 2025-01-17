```yaml
title:
  zh-CN: 基本用法
  en-US: Basic
```

## zh-CN

下拉菜单的基本用法。下拉菜单开启后会为触发元素添加 `arco-dropdown-open` 类名。

---

## en-US

Basic usage of the drop-down menu.

---

```vue
<template>
  <a-space size="large">
    <a-dropdown @select="handle">
      <a-button>Click Me</a-button>
      <template #content>
        <a-doption>Option 1</a-doption>
        <a-doption disabled>Option 2</a-doption>
        <a-doption :value="{ value: 'Option3' }">Option 3</a-doption>
      </template>
    </a-dropdown>
    <a-dropdown @select="handle" disabled>
      <a-button disabled>Click Me</a-button>
      <template #content>
        <a-doption>Option 1</a-doption>
        <a-doption disabled>Option 2</a-doption>
        <a-doption>Option 3</a-doption>
      </template>
    </a-dropdown>
    <a-dropdown @select="handle">
      <a-button>With Icon <icon-down/></a-button>
      <template #content>
        <a-doption>Option 1</a-doption>
        <a-doption disabled>Option 2</a-doption>
        <a-doption>Option 3</a-doption>
      </template>
    </a-dropdown>
  </a-space>
</template>

<script>
export default {
  methods:{
    handle(v) {
      console.log(v)
    }
  }
}
</script>

<style>
.arco-dropdown-open .arco-icon-down {
  transform: rotate(180deg);
}
</style>
```
