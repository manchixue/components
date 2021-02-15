---
category: cdk
type:
title: Portal
subtitle: 传送门
cover:
---

## 何时使用

当需要将元素传送到指定位置，但是不破坏当前 `v-dom` 的结构。

## API

### `ix-portal`

#### Props

| 名称       | 说明             | 类型                    | 默认值 | 备注                                                                                                                                                                                                  |
| ---------- | ---------------- | ----------------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `disabled` | 是否禁用传送     | `boolean`               | -      | 若禁用，则会以当前 `v-dom` 结构进行渲染                                                                                                                                                               |
| `target`   | 被传送的目标元素 | `string \| HTMLElement` | -      | 如果传入一个元素，组件直接传送到该元素上；如果是一个字符串，会根据是否创建过该元素，如果创建过直接读取缓存，否则在 `body` 的最后一个元素上创建元素，并将组件传送到该元素,传入的字符串将作为组件的类名 |