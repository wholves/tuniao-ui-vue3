# 图鸟UI Vue3 组件详细文档

## 完整组件API文档

### 1. TnButton - 按钮

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/button/src/button.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/button/src/button.vue`

**完整Props列表**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| width | 按钮宽度，默认单位 rpx | String \| Number | - | - |
| height | 按钮高度，默认单位 rpx | String \| Number | - | - |
| size | 按钮尺寸 | String | - | `sm` / `lg` / `xl` |
| shape | 按钮形状 | String | - | `circle` / `round` |
| type | 按钮颜色类型 | String | primary | `primary` / `success` / `warning` / `danger` / `info` |
| text | 文本按钮 | Boolean | false | true |
| plain | 朴素按钮 | Boolean | false | true |
| icon | 按钮图标 | String | - | 图标有效值 |
| bold | 字体加粗 | Boolean | false | true |
| font-size | 字体大小 | String | - | - |
| bg-color | 背景颜色 | String | - | - |
| text-color | 文字颜色 | String | - | - |
| border-bold | 边框加粗 | Boolean | false | true |
| border-color | 边框颜色 | String | - | - |
| shadow | 显示阴影 | Boolean | false | true |
| shadow-color | 阴影颜色 | String | - | - |
| hover-class | 点击触发的类 | String | tn-u-btn-hover | - |
| custom-style | 自定义样式 | CSSProperties | {} | - |
| custom-class | 自定义类名 | String | - | - |
| disabled | 禁用按钮 | Boolean | false | true |
| loading | 加载中 | Boolean | false | true |
| only-button | 纯按钮 | Boolean | false | true |
| debounce | 防抖 | Boolean | false | true |
| click-modifiers | 点击事件描述符 | String | - | `stop` |
| form-type | 表单事件类型 | String | - | `submit` / `reset` |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 按钮点击事件 | () => void |

---

### 2. TnIcon - 图标

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/icon/src/icon.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/icon/src/icon.vue`

**完整Props列表**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| name | 图标名称 | String | - | - |
| type | 图标颜色类型 | String | - | `primary` / `success` / `warning` / `danger` / `info` |
| color | 图标颜色 | String | - | - |
| size | 图标尺寸 | String \| Number | - | - |
| bold | 加粗图标 | Boolean | false | true |
| transparent | 透明图标 | Boolean | false | true |
| transparent-bg | 透明图标背景色 | String | - | - |
| img-mode | 图片模式 | String | aspectFit | - |
| offset-top | 垂直偏移量 | String \| Number | - | - |
| custom-style | 自定义样式 | Object | - | - |
| custom-class | 自定义类名 | String | - | - |

**Event**

| 事件名 | 说明 | 回调参数 |
|--------|------|----------|
| click | 点击图标触发 | - |

---

### 3. TnInput - 输入框

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/input/src/input.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/input/src/input.vue`

**完整Props列表**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | String \| Number | - | - |
| type | 输入框类型 | String | text | `number` / `idcard` / `digit` / `textarea` / `password` / `select` |
| disabled | 禁用 | Boolean | false | true |
| size | 尺寸 | String \| Number | - | `sm` / `lg` |
| height | 高度 | String \| Number | - | - |
| text-align | 文字对齐 | String | left | `right` |
| placeholder | 占位文本 | String | - | - |
| placeholder-style | 占位文本样式 | Object | - | - |
| border | 显示边框 | Boolean | true | false |
| border-color | 边框颜色 | String | - | - |
| underline | 下划线边框 | Boolean | false | true |
| maxlength | 最大长度 | Number | -1 | - |
| auto-height | 自动高度(textarea) | Boolean | true | false |
| confirm-type | 键盘确认按钮 | String | done | - |
| focus | 获取焦点 | Boolean | false | true |
| clearable | 清除按钮 | Boolean | false | true |
| show-password | 密码显示按钮 | Boolean | true | false |
| cursor-spacing | 光标与键盘距离 | Number | 0 | - |
| show-confirm-bar | 显示完成按钮栏 | Boolean | true | false |
| right-icon | 右侧图标 | String | - | - |
| trim | 去除两端空格 | Boolean | true | false |
| show-word-limit | 显示字数统计 | Boolean | false | true |
| word-limit-color | 字数统计颜色 | String | - | - |
| validate-event | 触发表单验证 | Boolean | true | false |
| custom-style | 自定义样式 | Object | - | - |
| custom-class | 自定义类名 | String | - | - |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| input | 输入事件 | (value: string \| number) => void |
| change | 值改变事件 | (value: string \| number) => void |
| click | 点击事件(select) | () => void |
| focus | 聚焦事件 | (e) => void |
| blur | 失焦事件 | (e) => void |
| clear | 清除事件 | () => void |
| confirm | 确认事件 | (value) => void |

**Slots**

| 插槽名 | 说明 |
|--------|------|
| prefix | 输入框前内容 |
| suffix | 输入框后内容 |

---

### 4. TnForm / TnFormItem - 表单

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/form/src/form.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/form/src/form.vue`

**TnForm Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model | 表单数据对象 | Object | - | - |
| rules | 表单校验规则 | Object \| Array | - | - |
| size | 控制表单内组件尺寸 | String | - | `sm` / `lg` |
| disabled | 禁用表单内所有组件 | Boolean | false | true |
| label-position | label标签位置 | String | right | `right` / `left` / `top` |
| require-asterisk-position | 必填星号位置 | String | left | `right` |
| hide-required-asterisk | 隐藏必填星号 | Boolean | false | true |
| label-width | label宽度 | String \| Number | - | - |
| label-suffix | label后缀 | String | - | - |
| status-icon | 显示校验图标 | Boolean | false | true |
| show-message | 显示校验结果 | Boolean | true | false |
| validate-on-rule-change | 规则改变立即校验 | Boolean | true | false |

**TnFormItem Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| label | label文本 | String | - | - |
| label-width | label宽度 | String \| Number | - | - |
| label-position | label位置 | String | right | `right` / `left` / `top` |
| prop | model的键名 | String \| Array | - | - |
| required | 必填项 | Boolean | false | true |
| rules | 校验规则 | Object \| Array | - | - |
| error | 错误信息 | String | - | - |
| show-message | 显示校验结果 | Boolean | true | false |
| size | 组件尺寸 | String | - | `sm` / `lg` |

**TnForm Methods**

| 方法名 | 说明 | 类型 |
|--------|------|------|
| validate | 验证整个表单 | (callback) => Promise |
| validateField | 验证指定字段 | (props, callback) => Promise |
| resetFields | 重置表单 | (props) => void |
| clearValidate | 清理校验信息 | (props) => void |

---

### 5. TnPopup - 弹出框

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/popup/src/popup.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/popup/src/popup.vue`

**完整Props列表**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 显示与隐藏 | Boolean | false | true |
| open-direction | 弹出方向 | String | center | `top` / `bottom` / `left` / `right` |
| width | 宽度 | String \| Number | - | - |
| height | 高度 | String \| Number | - | - |
| bg-color | 背景颜色 | String | #fff | - |
| radius | 圆角 | String \| Number | 15 | - |
| overlay | 显示遮罩 | Boolean | true | false |
| overlay-opacity | 遮罩透明度 | Number | 0.5 | - |
| overlay-closeable | 点击遮罩关闭 | Boolean | true | false |
| close-btn | 显示关闭按钮 | Boolean | false | true |
| close-btn-position | 关闭按钮位置 | String | right-top | `left-top` / `left-bottom` / `right-bottom` |
| safe-area-inset-bottom | 底部安全区域 | Boolean | true | false |
| z-index | zIndex | Number | 20075 | - |
| top | 距离顶部距离 | String \| Number | - | - |

**Event**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| open | 弹框打开事件 | () => void |
| close | 弹框关闭事件 | () => void |
| overlay-click | 遮罩点击事件 | () => void |

**Slots**

| 插槽名 | 说明 |
|--------|------|
| default | 自定义弹框内容 |
| closeBtn | 自定义关闭按钮 |

---

### 6. TnModal - 模态框

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/modal/src/modal.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/modal/src/modal.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| z-index | zIndex | Number | 20076 |

**showModal函数配置项**

| 属性名 | 说明 | 类型 | 必填 |
|--------|------|------|------|
| content | 内容 | String | 是 |
| title | 标题 | String | 否 |
| showCancel | 显示取消按钮 | Boolean | 否 |
| cancelText | 取消按钮文字 | String | 否 |
| cancelStyle | 取消按钮样式 | Object | 否 |
| confirmText | 确认按钮文字 | String | 否 |
| confirmStyle | 确认按钮样式 | Object | 否 |
| mask | 显示遮罩 | Boolean | 否 |
| maskClosable | 点击遮罩关闭 | Boolean | 否 |
| cancel | 取消回调 | Function | 否 |
| confirm | 确认回调 | Function | 否 |

**使用示例**
```vue
<script setup>
import { ref } from 'vue'
const modalRef = ref()

const openModal = () => {
  modalRef.value?.showModal({
    title: '操作提示',
    content: 'Modal内容',
    showCancel: true,
    cancel: () => {
      console.log('点击了取消')
    },
    confirm: () => {
      console.log('点击了确认')
    }
  })
}
</script>

<template>
  <TnButton @click="openModal">显示模态框</TnButton>
  <TnModal ref="modalRef" />
</template>
```

---

### 7. TnActionSheet - 操作菜单

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/action-sheet/src/action-sheet.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/action-sheet/src/action-sheet.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| z-index | zIndex | Number | 20076 |

**show函数配置项**

| 属性名 | 说明 | 类型 | 必填 |
|--------|------|------|------|
| actions | 选项内容数据 | Array | 是 |
| title | 弹框标题 | String | 否 |
| cancelText | 取消按钮文字 | String | 否 |
| mask | 显示遮罩 | Boolean | 否 |
| maskClosable | 点击遮罩关闭 | Boolean | 否 |
| cancel | 取消回调 | Function | 否 |
| select | 选项点击回调 | Function | 否 |

**使用示例**
```vue
<script setup>
import { ref } from 'vue'
const actionSheetRef = ref()

const openActionSheet = () => {
  actionSheetRef.value?.show({
    actions: [
      { text: '选项1', value: '1' },
      { text: '选项2', value: '2', desc: '暂时不能选' },
      { text: '选项3', value: '3' },
    ],
  })
}
</script>

<template>
  <TnButton @click="openActionSheet">显示操作菜单</TnButton>
  <TnActionSheet ref="actionSheetRef" />
</template>
```

---

### 8. TnNotify - 消息通知

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/notify/src/notify.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/notify/src/notify.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| z-index | zIndex | Number | 20074 |
| offset-top | 距离顶部距离 | Number | 0 |

**show函数配置参数**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 | 必填 |
|--------|------|------|--------|--------|------|
| msg | 消息内容 | String | - | - | 是 |
| type | 消息类型 | String | primary | `success` / `warning` / `danger` / `info` | 否 |
| position | 通知位置 | String | top | `center` / `bottom` | 否 |
| bgColor | 背景颜色 | String | - | - | 否 |
| textColor | 字体颜色 | String | - | - | 否 |
| duration | 自动关闭时间 | Number | 3000 | - | 否 |

---

### 9. TnTabs / TnTabsItem - 标签栏

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/tabs/src/tabs.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/tabs/src/tabs.vue`

**TnTabs Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 当前选中索引 | String \| Number | - | - |
| height | 标签栏高度 | String | 80rpx | - |
| bar-width | 滑块宽度 | String | 40rpx | - |
| bg-color | 背景颜色 | String | - | - |
| bar-color | 滑块颜色 | String | - | - |
| color | 默认颜色 | String | - | - |
| active-color | 选中颜色 | String | - | - |
| font-size | 文字大小 | String | - | - |
| active-font-size | 激活文字大小 | String | - | - |
| bottom-shadow | 显示底部阴影 | Boolean | true | false |
| scroll | 可滚动 | Boolean | true | false |
| bar | 显示滑块 | Boolean | true | false |
| active-bold | 激活加粗 | Boolean | true | false |
| offset-top | 距离顶部距离 | Number | 0 | - |
| before-switch | 切换前回调 | Function | - | - |

**TnTabsItem Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| name | 唯一标识 | String \| Number | - |
| title | 显示文本 | String | - |
| badge-config | 角标配置 | Object | - |
| disabled | 禁止选择 | Boolean | false |
| color | 默认颜色 | String | - |
| active-color | 选中颜色 | String | - |
| font-size | 文字大小 | String | - |
| active-font-size | 激活文字大小 | String | - |

---

### 10. TnSwiper - 轮播图

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/swiper/src/swiper.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/swiper/src/swiper.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 当前选中索引 | Number | 0 | - |
| data | 轮播数据 | Array | [] | - |
| blank-count | 空白swiper数量 | Number | - | - |
| width | 轮播图宽度 | String | - | - |
| height | 轮播图高度 | String | - | - |
| autoplay | 自动播放 | Boolean | false | true |
| interval | 自动播放间隔(ms) | Number | 5000 | - |
| duration | 动画时长(ms) | Number | 500 | - |
| loop | 循环播放 | Boolean | false | true |
| previous-margin | 前边距 | String | 0px | - |
| next-margin | 后边距 | String | 0px | - |
| indicator | 显示指示器 | Boolean | false | true |
| indicator-position | 指示器位置 | String | center-bottom | - |
| indicator-type | 指示器类型 | String | dot | `line` / `number` |
| indicator-bg-color | 指示器颜色 | String | - | - |
| indicator-active-bg-color | 指示器激活颜色 | String | - | - |
| indicator-text-color | 指示器文本颜色 | String | - | - |

---

### 11. TnNavbar - 顶部导航栏

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/navbar/src/navbar.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/navbar/src/navbar.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| height | 导航栏高度 | String | - | - |
| bg-color | 背景颜色 | String | - | - |
| text-color | 文字颜色 | String | - | - |
| frosted | 毛玻璃效果 | Boolean | false | true |
| opacity | 透明度 | Number | 1 | - |
| back-icon | 返回按钮图标 | String | left | - |
| back-text | 返回按钮文字 | String | - | - |
| home-icon | 返回首页图标 | String | home-capsule-fill | - |
| bottom-shadow | 显示底部阴影 | Boolean | true | false |
| safe-area-inset-right | 预留右边安全距离 | Boolean | true | false |
| center | 居中显示内容 | Boolean | true | false |
| right-operation-width | 右边操作区域宽度 | String | - | - |
| before-back | 返回前回调 | Function | - | - |
| before-home | 返回首页前回调 | Function | - | - |
| index-url | 首页地址 | String | /pages/index/index | - |
| fixed | 固定在顶部 | Boolean | false | true |
| placeholder | 固定后开启占位 | Boolean | true | false |
| z-index | zIndex | Number | 20090 | - |

**Slots**

| 插槽名 | 说明 |
|--------|------|
| default | 导航栏内容 |
| back | 返回区域内容 |
| right | 右边操作区域内容 |

---

### 12. TnTabbar / TnTabbarItem - 底部导航栏

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/tabbar/src/tabbar.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/tabbar/src/tabbar.vue`

**TnTabbar Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 当前选中索引 | String \| Number | - | - |
| height | 导航栏高度 | String | - | - |
| bulge-max-size | 凸起按钮最大尺寸 | Number | 80 | - |
| bulge-size-percent | 凸起按钮尺寸比例 | Number | 0.75 | - |
| bg-color | 背景颜色 | String | - | - |
| frosted | 毛玻璃效果 | Boolean | false | true |
| inactive-color | 未选中颜色 | String | - | - |
| active-color | 选中颜色 | String | - | - |
| icon-size | 图标大小 | String | - | - |
| font-size | 文字大小 | String | - | - |
| top-shadow | 显示顶部阴影 | Boolean | true | false |
| switch-animation | 切换动画 | Boolean | false | true |
| fixed | 固定在底部 | Boolean | false | true |
| safe-area-inset-bottom | 底部安全边距 | Boolean | true | false |
| placeholder | 固定后开启占位 | Boolean | true | false |
| before-switch | 切换前回调 | Function | - | - |
| z-index | zIndex | Number | 20090 | - |
| hidden-fixed-tabbar | 隐藏固定导航栏 | Boolean | false | true |

**TnTabbarItem Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| name | 唯一值 | String \| Number | - |
| icon | 默认图标 | String | - |
| active-icon | 选中图标 | String | - |
| text | 显示文本 | String | - |
| inactive-color | 未选中颜色 | String | - |
| active-color | 选中颜色 | String | - |
| icon-size | 图标大小 | String | - |
| font-size | 文字大小 | String | - |
| bulge | 凸起显示 | Boolean | false |
| bulge-bg-color | 凸起背景色 | String | - |
| bulge-text-color | 凸起文字色 | String | - |
| badge | 角标内容 | String \| Number | - |
| badge-config | 角标配置 | Object | - |
| disabled | 禁止点击 | Boolean | false |

---

### 13. TnCalendar - 日历

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/calendar/src/calendar.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/calendar/src/calendar.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定日期值 | String \| Array | - | - |
| mode | 日历模式 | String | date | `multi` / `range` |
| min-date | 最小日期 | String \| Number | - | - |
| max-date | 最大日期 | String \| Number | - | - |
| active-bg-color | 选中背景色 | String | - | - |
| active-text-color | 选中文字色 | String | - | - |
| range-bg-color | 范围背景色 | String | - | - |
| range-text-color | 范围文字色 | String | - | - |
| allow-change-year | 允许切换年份 | Boolean | true | false |
| allow-change-month | 允许切换月份 | Boolean | true | false |
| show-lunar | 显示农历 | Boolean | false | true |
| range-start-desc | 范围开始文案 | String | 开始 | - |
| range-end-desc | 范围结束文案 | String | 结束 | - |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 日期改变事件 | (value) => void |
| change-year | 切换年份事件 | (value) => void |
| change-month | 切换月份事件 | (value) => void |

---

### 14. TnPicker - 选择器

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/picker/src/picker.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/picker/src/picker.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | Array \| String \| Number | - | - |
| open/v-model:open | 显示与隐藏 | Boolean | false | true |
| data | 选项数据 | Array | - | - |
| immediate-change | 立即触发change | Boolean | true | false |
| allow-confirm-before-scroll-end | 允许滑动前确认 | Boolean | false | true |
| indicator-height | indicator高度(px) | Number | 44 | - |
| label-key | label属性名 | String | label | - |
| value-key | value属性名 | String | value | - |
| children-key | children属性名 | String | children | - |
| show-cancel | 显示取消按钮 | Boolean | true | false |
| cancel-text | 取消按钮文本 | String | 取消 | - |
| cancel-color | 取消按钮颜色 | String | - | - |
| show-confirm | 显示确认按钮 | Boolean | true | false |
| confirm-text | 确认按钮文本 | String | 确定 | - |
| confirm-color | 确认按钮颜色 | String | - | - |
| mask | 显示遮罩 | Boolean | false | true |
| z-index | zIndex | Number | 20075 | - |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 选项改变 | (value, index, item) => void |
| confirm | 点击确认 | (value, item) => void |
| cancel | 点击取消 | () => void |
| close | 弹框关闭 | () => void |
| pickstart | 开始滚动 | () => void |
| pickend | 结束滚动 | () => void |

**Expose**

| 函数名 | 说明 | 类型 |
|--------|------|------|
| resetPickerViewIndex | 重置选择器值 | () => void |
| resetPickerIndexWithPosition | 重置指定范围值 | (start, end) => void |

---

### 15. TnDateTimePicker - 日期时间选择器

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/date-time-picker/src/date-time-picker.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/date-time-picker/src/date-time-picker.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | String | - | - |
| open/v-model:open | 显示与隐藏 | Boolean | false | true |
| mode | 选择器类型 | String | date | `year` / `yearmonth` / `datetime` / `time` / `datetimeNoSecond` / `timeNoSecond` |
| min-time | 最小时间 | String | - | - |
| max-time | 最大时间 | String | - | - |
| init-current-date-time | 初始化当前时间 | Boolean | true | false |
| format | 日期格式化 | String | YYYY/MM/DD HH:mm:ss | - |
| show-cancel | 显示取消按钮 | Boolean | true | false |
| cancel-text | 取消按钮文本 | String | 取消 | - |
| cancel-color | 取消按钮颜色 | String | - | - |
| show-confirm | 显示确认按钮 | Boolean | true | false |
| confirm-text | 确认按钮文本 | String | 确定 | - |
| confirm-color | 确认按钮颜色 | String | - | - |
| mask | 显示遮罩 | Boolean | false | true |
| z-index | zIndex | Number | 20075 | - |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 日期时间改变 | (value) => void |
| confirm | 点击确认 | (value) => void |
| cancel | 点击取消 | () => void |
| close | 弹框关闭 | () => void |

---

### 16. TnRegionPicker - 地区选择器

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/region-picker/src/region-picker.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/region-picker/src/region-picker.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | String[] | - |
| open/v-model:open | 显示与隐藏 | Boolean | false |
| show-cancel | 显示取消按钮 | Boolean | true |
| cancel-text | 取消按钮文本 | String | 取消 |
| cancel-color | 取消按钮颜色 | String | - |
| show-confirm | 显示确认按钮 | Boolean | true |
| confirm-text | 确认按钮文本 | String | 确定 |
| confirm-color | 确认按钮颜色 | String | - |
| mask | 显示遮罩 | Boolean | false |
| z-index | zIndex | Number | 20075 |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 地区改变 | (value, item) => void |
| confirm | 点击确认 | (value, item) => void |
| cancel | 点击取消 | () => void |
| close | 弹框关闭 | () => void |

---

### 17. TnCheckbox / TnCheckboxGroup - 复选框

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/checkbox/src/checkbox.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/checkbox/src/checkbox.vue`

**TnCheckbox Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | String \| Number \| Boolean | - | - |
| label | 复选框的值 | String \| Number | - | - |
| indeterminate | 不确定状态 | Boolean | false | true |
| active-value | 选中值 | String \| Number \| Boolean | true | - |
| inactive-value | 未选中值 | String \| Number \| Boolean | false | - |
| size | 尺寸 | String | - | `sm` / `lg` |
| checked-shape | 选框形状 | String | square | `circle` |
| disabled | 禁用 | Boolean | false | true |
| label-disabled | 禁止点击标签 | Boolean | false | true |
| border | 显示边框 | Boolean | false | true |
| active-color | 激活颜色 | String | - | - |
| custom-style | 自定义样式 | CSSProperties | {} | - |
| custom-class | 自定义类名 | String | - | - |
| validate-event | 触发表单验证 | Boolean | true | false |

**TnCheckboxGroup Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | Array | - |
| size | 尺寸 | String | - |
| checked-shape | 选框形状 | String | square |
| disabled | 禁用 | Boolean | false |
| label-disabled | 禁止点击标签 | Boolean | false |
| border | 显示边框 | Boolean | false |
| active-color | 激活颜色 | String | - |
| min | 最小勾选数 | Number | - |
| max | 最大勾选数 | Number | - |
| wrap | 独占一行 | Boolean | false |
| validate-event | 触发表单验证 | Boolean | true |

---

### 18. TnRadio / TnRadioGroup - 单选框

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/radio/src/radio.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/radio/src/radio.vue`

**TnRadio Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | String \| Number \| Boolean | - |
| label | 单选框的值 | String \| Number \| Boolean | - |
| size | 尺寸 | String | - |
| disabled | 禁用 | Boolean | false |
| label-disabled | 禁止点击标签 | Boolean | false |
| border | 显示边框 | Boolean | false |
| active-color | 激活颜色 | String | - |
| custom-style | 自定义样式 | CSSProperties | {} |
| custom-class | 自定义类名 | String | - |

**TnRadioGroup Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | String \| Number \| Boolean | - |
| size | 尺寸 | String | - |
| disabled | 禁用 | Boolean | false |
| label-disabled | 禁止点击标签 | Boolean | false |
| border | 显示边框 | Boolean | false |
| active-color | 激活颜色 | String | - |
| wrap | 独占一行 | Boolean | false |
| validate-event | 触发表单验证 | Boolean | true |

---

### 19. TnSwitch - 开关

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/switch/src/switch.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/switch/src/switch.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | String \| Number \| Boolean | - | - |
| shape | 开关形状 | String | round | `square` |
| size | 开关尺寸 | String | - | `sm` / `lg` |
| width | 开关宽度 | String \| Number | - | - |
| disabled | 禁用 | Boolean | false | true |
| loading | 加载状态 | Boolean | false | true |
| inactive-color | 未选中颜色 | String | - | - |
| active-color | 选中颜色 | String | - | - |
| inactive-text | 未选中文本 | String | - | - |
| active-text | 选中文本 | String | - | - |
| inactive-icon | 未选中图标 | String | - | - |
| active-icon | 选中图标 | String | - | - |
| inactive-value | 未选中值 | String \| Number \| Boolean | false | - |
| active-value | 选中值 | String \| Number \| Boolean | true | - |
| custom-style | 自定义样式 | CSSProperties | {} | - |
| custom-class | 自定义类名 | String | - | - |
| validate-event | 触发表单验证 | Boolean | true | false |
| before-change | 状态改变前钩子 | Function | - | - |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 状态改变 | (value) => void |

---

### 20. TnSlider - 滑动条

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/slider/src/slider.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/slider/src/slider.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | Number \| Number[] | - |
| size | 尺寸 | String | - |
| slider-bar-size | 滑块尺寸 | String \| Number | - |
| slider-height | 滑动条高度 | String \| Number | - |
| active-color | 激活颜色 | String | - |
| inactive-color | 未激活颜色 | String | - |
| disabled | 禁用 | Boolean | false |
| step | 步进值 | Number | 1 |
| min | 最小值 | Number | 1 |
| max | 最大值 | Number | 100 |
| validate-event | 触发表单验证 | Boolean | true |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 值改变(手指离开时) | (value) => void |
| input | 值改变(实时) | (value) => void |

---

### 21. TnNumberBox - 步进器

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/number-box/src/number-box.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/number-box/src/number-box.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | Number | - |
| size | 尺寸 | String | - |
| width | 宽度 | String \| Number | - |
| height | 高度 | String \| Number | - |
| font-size | 字体大小 | String \| Number | - |
| bg-color | 背景颜色 | String | - |
| text-color | 字体颜色 | String | - |
| min | 最小值 | Number | 0 |
| max | 最大值 | Number | 100 |
| step | 步进值 | Number | 1 |
| disabled | 禁用 | Boolean | false |
| input-disabled | 禁止输入 | Boolean | false |
| input-spacing | 输入框与键盘间距 | Number | 20 |
| long-press | 长按递增减 | Boolean | true |
| long-press-interval | 长按间隔时间 | Number | 250 |
| validate-event | 触发表单验证 | Boolean | true |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 值改变 | (value) => void |
| input | 输入值改变 | (value) => void |

**Slots**

| 插槽名 | 说明 |
|--------|------|
| minus | 减按钮内容 |
| plus | 加按钮内容 |

---

### 22. TnRate - 评分

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/rate/src/rate.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/rate/src/rate.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | Number | 0 | - |
| min | 最小值 | Number | 0 | - |
| max | 最大值 | Number | 5 | - |
| allow-half | 允许半选 | Boolean | false | true |
| readonly | 只读 | Boolean | false | true |
| size | 尺寸 | String | - | `sm` / `lg` / `xl` |
| inactive-icon | 未选中图标 | String | star | - |
| active-icon | 选中图标 | String | star-fill | - |
| inactive-color | 未选中颜色 | String | - | - |
| active-color | 选中颜色 | String | - | - |
| gutter | 图标间距 | String | - | - |
| custom-data | 自定义指定位置图标 | Object | - | - |
| validate-event | 触发表单验证 | Boolean | true | false |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 值改变 | (value) => void |

---

### 23. TnTag - 标签

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/tag/src/tag.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/tag/src/tag.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| width | 标签宽度 | String \| Number | - | - |
| height | 标签高度 | String \| Number | - | - |
| size | 标签尺寸 | String | - | `sm` / `lg` / `xl` |
| shape | 标签形状 | String | - | `circle` / `round` / `text` |
| type | 颜色类型 | String | - | `primary` / `success` / `warning` / `danger` / `info` |
| bold | 字体加粗 | Boolean | false | true |
| font-size | 字体大小 | String | - | - |
| bg-color | 背景颜色 | String | - | - |
| text-color | 文字颜色 | String | - | - |
| border | 显示边框 | Boolean | false | true |
| border-bold | 边框加粗 | Boolean | false | true |
| border-color | 边框颜色 | String | - | - |
| custom-style | 自定义样式 | CSSProperties | {} | - |
| custom-class | 自定义类名 | String | - | - |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 标签点击事件 | () => void |

---

### 24. TnAvatar / TnAvatarGroup - 头像

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/avatar/src/avatar.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/avatar/src/avatar.vue`

**TnAvatar Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| url | 头像地址 | String | - | - |
| icon | 头像图标 | String | - | - |
| icon-config | 图标配置 | Object | {} | - |
| size | 头像尺寸 | String | - | `sm` / `lg` / `xl` |
| shape | 头像形状 | String | circle | `square` |
| type | 颜色类型 | String | - | `primary` / `success` / `warning` / `danger` / `info` |
| img-mode | 图片显示模式 | String | aspectFit | - |
| bg-color | 背景颜色 | String | - | - |
| border | 显示边框 | Boolean | false | true |
| border-bold | 边框加粗 | Boolean | false | true |
| border-color | 边框颜色 | String | - | - |
| shadow | 显示阴影 | Boolean | false | true |
| shadow-color | 阴影颜色 | String | - | - |
| badge | 角标内容 | String \| Number | - | - |
| badge-config | 角标配置 | Object | {} | - |

**TnAvatarGroup Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| icon-config | 图标配置 | Object | {} |
| size | 头像尺寸 | String | - |
| shape | 头像形状 | String | circle |
| type | 颜色类型 | String | - |
| img-mode | 图片显示模式 | String | aspectFit |
| bg-color | 背景颜色 | String | - |
| border | 显示边框 | Boolean | true |
| border-bold | 边框加粗 | Boolean | false |
| border-color | 边框颜色 | String | tn-white |
| shadow | 显示阴影 | Boolean | false |
| shadow-color | 阴影颜色 | String | - |
| gap | 头像间遮挡比例 | String \| Number | 0.4 |

---

### 25. TnBadge - 徽标

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/badge/src/badge.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/badge/src/badge.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| value | 徽标内容 | String \| Number | - | - |
| max | 徽标最大值 | String \| Number | - | - |
| type | 颜色类型 | String | primary | `success` / `warning` / `danger` / `info` |
| bg-color | 背景颜色 | String | - | - |
| text-color | 文字颜色 | String | - | - |
| size | 徽标尺寸 | String \| Number | - | `lg` / `xl` |
| font-size | 字体大小 | String \| Number | - | - |
| bold | 字体加粗 | Boolean | false | true |
| custom-style | 自定义样式 | Object | - | - |
| custom-class | 自定义类名 | String | - | - |
| dot | 显示点徽标 | Boolean | false | true |
| absolute | 绝对定位 | Boolean | false | true |
| absolute-position | 绝对定位位置 | Object | {} | - |
| absolute-center | 居中显示 | Boolean | false | true |
| index | 点击标识 | String \| Number | - | - |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 徽标点击事件 | () => void |

---

### 26. TnTitle - 标题

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/title/src/title.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/title/src/title.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| title | 标题内容 | String | - | - |
| sub-title | 子标题内容 | String | - | - |
| mode | 标题模式 | String | normal | `vLine` / `dot` / `hLine` / `subTitle` / `transparent` |
| size | 标题尺寸 | String | - | `sm` / `lg` / `xl` |
| align | 标题对齐 | String | left | `center` / `right` |
| color | 标题颜色 | String | - | - |
| assist-color | 辅助元素颜色 | String | - | - |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 点击事件 | () => void |

---

### 27. TnLineProgress / TnCircleProgress - 进度条

**组件位置**
- node: 
  - `@tuniao/tnui-vue3-uniapp/components/line-progress/src/line-progress.vue`
  - `@tuniao/tnui-vue3-uniapp/components/circle-progress/src/circle-progress.vue`
- uni_modules:
  - `@/uni_modules/tuniaoui-vue3/components/line-progress/src/line-progress.vue`
  - `@/uni_modules/tuniaoui-vue3/components/circle-progress/src/circle-progress.vue`

**通用Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| percent | 进度值(0-100) | Number | 0 |
| active-color | 已完成颜色 | String | - |
| inactive-color | 未完成颜色 | String | - |
| show-percent | 显示进度值 | Boolean | false |
| duration | 动画时长(ms) | Number | 1500 |

**LineProgress 特有Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| height | 进度条高度 | String \| Number | 20 |
| stripe | 显示条纹 | Boolean | false |
| stripe-animated | 条纹动画 | Boolean | true |

**CircleProgress 特有Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| radius | 圆半径(px) | Number | 50 |
| ring-width | 圆环宽度(px) | Number | 7 |

**Slots**

| 插槽名 | 说明 |
|--------|------|
| default | 自定义进度内容 |

---

### 28. TnLoading - 加载图标

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/loading/src/loading.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/loading/src/loading.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| show | 显示加载图标 | Boolean | false | true |
| animation | 显示动画 | Boolean | false | true |
| mode | 加载模式 | String | circle | `flower` / `semicircle` |
| type | 颜色类型 | String | primary | `success` / `warning` / `danger` / `info` |
| color | 颜色 | String | - | - |
| size | 大小 | String \| Number | - | `sm` / `lg` / `xl` |
| duration | 动画时间(秒) | String \| Number | - | - |
| time-function | 动画执行函数 | String | - | - |

---

### 29. TnLoadmore - 加载更多

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/loadmore/src/loadmore.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/loadmore/src/loadmore.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| status | 加载状态 | String | loadmore | `loading` / `nomore` / `empty` |
| size | 内容尺寸 | String | - | `sm` / `lg` / `xl` |
| color | 内容颜色 | String | - | - |
| text | 加载文案配置 | Object | - | - |
| loading-icon | 显示加载图标 | Boolean | true | false |
| loading-icon-mode | 加载图标类型 | String | circle | `flower` / `semicircle` |
| loading-text | 显示加载文案 | Boolean | true | false |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 点击事件 | () => void |

---

### 30. TnEmpty - 空白页

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/empty/src/empty.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/empty/src/empty.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| mode | 空白提示类型 | String | - | `cart` / `page` / `search` / `address` / `network` / `order` / `coupon` / `favor` / `permission` / `history` / `message` / `list` / `data` / `comment` |
| color | 内容颜色 | String | - | - |
| size | 内容大小 | String | - | `sm` / `lg` / `xl` |
| show-tips | 显示空白提示 | Boolean | true | false |

**Slots**

| 插槽名 | 说明 |
|--------|------|
| icon | 自定义图标内容 |
| tips | 自定义提示文字 |

---

### 31. TnSearchBox - 搜索框

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/search-box/src/search-box.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/search-box/src/search-box.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 绑定值 | String | - | - |
| placeholder | 占位内容 | String | 请输入搜索内容 | - |
| placeholder-icon | 占位图标 | String | search | - |
| shape | 搜索框形状 | String | square | `round` |
| size | 搜索框尺寸 | String | - | `sm` / `lg` / `xl` |
| text-color | 文字颜色 | String | - | - |
| placeholder-color | 占位文字颜色 | String | - | - |
| text-align | 文字对齐 | String | left | `center` / `right` |
| border | 显示边框 | Boolean | true | false |
| border-color | 边框颜色 | String | - | - |
| focus | 获取焦点 | Boolean | false | true |
| disabled | 禁用 | Boolean | false | true |
| clearable | 显示清除按钮 | Boolean | true | false |
| search-button | 显示搜索按钮 | Boolean | true | false |
| search-button-text | 搜索按钮文字 | String | 搜索 | - |
| search-button-text-color | 搜索按钮文字颜色 | String | - | - |
| search-button-bg-color | 搜索按钮背景色 | String | - | - |
| throllte | 输入节流 | Boolean | true | false |
| throllte-time | 节流延迟时间 | Number | 1000 | - |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 输入改变 | (value) => void |
| input | 输入时触发 | (value) => void |
| click | 搜索框点击 | () => void |
| focus | 聚焦 | () => void |
| blur | 失焦 | () => void |
| search | 点击搜索按钮 | (value) => void |
| clear | 点击清除按钮 | () => void |

---

### 32. TnOverlay - 遮罩层

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/overlay/src/overlay.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/overlay/src/overlay.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| show/v-model:show | 显示与隐藏 | Boolean | false |
| duration | 动画时间(ms) | Number | 300 |
| opacity | 透明度(0-1) | Number | 0.5 |
| z-index | zIndex | Number | 9999 |

**Events**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 遮罩层点击 | () => void |

**Slots**

| 插槽名 | 说明 |
|--------|------|
| default | 自定义遮罩内容 |

---

### 33. TnNoticeBar - 通知栏

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/notice-bar/src/notice-bar.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/notice-bar/src/notice-bar.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| show | 显示通知栏 | Boolean | true | false |
| data | 通知栏数据 | String[] | - | - |
| bg-color | 背景颜色 | String | - | - |
| text-color | 文字颜色 | String | - | - |
| font-size | 文字大小 | String | - | - |
| left-icon | 左边图标 | String | - | - |
| left-icon-color | 左图标颜色 | String | - | - |
| left-icon-size | 左图标大小 | String | - | - |
| right-icon | 右边图标 | String | - | - |
| right-icon-color | 右图标颜色 | String | - | - |
| right-icon-size | 右图标大小 | String | - | - |
| pause | 暂停播放 | Boolean | false | true |
| auto-play | 自动播放 | Boolean | true | false |
| direction | 滚动方向 | String | horizontal | `vertical` |
| loop | 循环播放 | Boolean | true | false |
| speed | 播放速度 | Number | - | - |
| auto-hide | data为空自动隐藏 | Boolean | true | false |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 通知点击 | (index) => void |
| left-icon-click | 左图标点击 | () => void |
| right-icon-click | 右图标点击 | () => void |

---

### 34. TnSteps / TnStepsItem - 步骤条

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/steps/src/steps.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/steps/src/steps.vue`

**TnSteps Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 当前选中步骤 | String \| Number | - | - |
| mode | 步骤条模式 | String | dot | `number` / `dotIcon` / `icon` |
| color | 默认颜色 | String | - | - |
| active-color | 激活颜色 | String | - | - |
| disabled | 禁止点击 | Boolean | false | true |

**TnStepsItem Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| title | 显示文本 | String | - |
| icon | 默认图标 | String | - |
| active-icon | 激活图标 | String | - |
| color | 默认颜色 | String | - |
| active-color | 激活颜色 | String | - |
| disabled | 禁止点击 | Boolean | false |

**TnSteps Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 步骤改变 | (index) => void |

**TnStepsItem Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 步骤点击 | () => void |

---

### 35. TnSubsection / TnSubsectionItem - 分段器

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/subsection/src/subsection.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/subsection/src/subsection.vue`

**TnSubsection Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 绑定索引值 | Number | 0 | - |
| mode | 分段器模式 | String | default | `button` |
| size | 分段器尺寸 | String | - | `sm` / `lg` / `xl` |
| radius | 圆角值 | String | 8 | - |
| disabled | 禁止选择 | Boolean | false | true |
| active-color | 激活颜色 | String | - | - |

**TnSubsectionItem Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| title | 文本内容 | String | - |
| disabled | 禁止选择 | Boolean | false |
| active-color | 激活颜色 | String | - |

**TnSubsection Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 分段器改变 | (index) => void |

**TnSubsectionItem Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 点击事件 | (title) => void |

---

### 36. TnCollapse / TnCollapseItem - 折叠面板

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/collapse/src/collapse.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/collapse/src/collapse.vue`

**TnCollapse Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 当前展开标识 | String \| Number \| Array | - |
| accordion | 手风琴效果 | Boolean | true |
| show-arrow | 显示箭头 | Boolean | true |
| arrow-color | 箭头颜色 | String | - |

**TnCollapseItem Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| title | 标题 | String | - |
| disabled | 禁止操作 | Boolean | false |

**TnCollapse Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 折叠状态改变 | (value) => void |

**TnCollapseItem Slots**

| 插槽名 | 说明 |
|--------|------|
| default | 折叠显示内容 |
| title | 自定义标题 |

---

### 37. TnSwipeAction / TnSwipeActionItem - 滑动菜单

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/swipe-action/src/swipe-action.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/swipe-action/src/swipe-action.vue`

**TnSwipeAction Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| exclusive | 只允许一个打开 | Boolean | true |
| auto-close | 自动关闭菜单 | Boolean | true |

**TnSwipeActionItem Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| options | 菜单配置项 | Array | - |
| auto-close | 自动关闭菜单 | Boolean | true |
| disabled | 禁用 | Boolean | false |
| threshold | 滑动阈值(px) | Number | 20 |

**TnSwipeAction Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| open | 菜单打开 | (index) => void |
| select | 选项选中 | (index, optionIndex) => void |

---

### 38. TnCountDown - 倒计时

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/count-down/src/count-down.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/count-down/src/count-down.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| time | 倒计时时间(秒) | Number | 0 | - |
| auto-start | 自动开始 | Boolean | true | false |
| size | 倒计时尺寸 | String | - | `sm` / `lg` / `xl` |
| text-color | 文字颜色 | String | - | - |
| show-day | 显示天数 | Boolean | false | true |
| show-hour | 显示小时 | Boolean | true | false |
| show-minute | 显示分钟 | Boolean | true | false |
| show-second | 显示秒数 | Boolean | true | false |
| auto-hide-day | 自动隐藏天数 | Boolean | true | false |
| separator-mode | 分割符类型 | String | en | `cn` |
| separator-color | 分割符颜色 | String | - | - |
| border | 显示边框 | Boolean | false | true |
| border-color | 边框颜色 | String | - | - |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| start | 倒计时开始 | () => void |
| end | 倒计时结束 | () => void |

**Expose**

| 函数名 | 说明 | 类型 |
|--------|------|------|
| start | 开始倒计时 | () => void |
| stop | 停止倒计时 | () => void |
| reset | 重置倒计时 | () => void |

---

### 39. TnCountTo - 数字跳转

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/count-to/src/count-to.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/count-to/src/count-to.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| start | 开始值 | String \| Number | 0 |
| end | 结束值 | String \| Number | - |
| text-color | 文字颜色 | String | - |
| font-size | 字体大小 | String | - |
| decimals | 小数位数 | Number | 0 |
| decimal-separator | 小数点分隔符 | String | . |
| thousands-separator | 千分位分隔符 | String | - |
| duration | 动画时长(ms) | Number | 1500 |

**Emits**

| 事件名 | 说明 | 类型 |
|--------|------|------|
| end | 数字变化结束 | () => void |

---

### 40. TnCountScroll - 数字滚动

**组件位置**
- node: `@tuniao/tnui-vue3-uniapp/components/count-scroll/src/count-scroll.vue`
- uni_modules: `@/uni_modules/tuniaoui-vue3/components/count-scroll/src/count-scroll.vue`

**Props**

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| value | 待显示的值 | String \| Number | - |
| text-color | 文字颜色 | String | - |
| font-size | 字体大小 | String | - |
| decimal-separator | 小数点分隔符 | String | . |
| thousands-separator | 千分位分隔符 | String | , |
| duration | 动画时长(ms) | Number | 1500 |

---

## 更多组件

由于文档篇幅较长，以下是其他组件的简要说明：

### 41. TnSticky - 吸顶组件
用于将组件固定在顶部

### 42. TnWeekCalendar - 周日历
用于选择一个星期日期

### 43. TnKeyboard - 软键盘
用于输入指定内容（密码、手机号等）

### 44. TnImageUpload - 图片上传
用于上传图片场景

### 45. TnListItem - 列表
用于展示列表数据

### 46. TnPhotoAlbum - 相册
用于展示图片列表

### 47. TnWaterFall - 瀑布流
用于展示等宽不等高元素

### 48. TnScrollList - 横向滚动
用于展示横向滚动列表

### 49. TnIndexList - 索引列表
用于展示带索引的列表

### 50. TnReadMore - 阅读更多
用于收起长文本

### 51. TnSwitchTab - 选项卡切换
用于点击选项切换内容

### 52. TnBubbleBox - 气泡弹框
用于弹出附加选项

### 53. TnFooter - 页脚
用于展示页脚信息

### 54. TnLazyLoad - 懒加载
用于延迟加载图片

---

## 总结

图鸟UI Vue3 提供了完整的组件库，涵盖了：
- ✅ 基础组件（按钮、图标、标签等）
- ✅ 表单组件（输入框、选择器、开关等）
- ✅ 反馈组件（弹窗、提示、通知等）
- ✅ 导航组件（顶部导航、底部导航、标签栏等）
- ✅ 展示组件（轮播图、进度条、步骤条等）
- ✅ 布局组件（列表、折叠面板、瀑布流等）
- ✅ 日历组件（日历、周日历等）

所有组件均支持：
- 🎨 丰富的样式自定义选项
- 📱 多平台适配（App、H5、微信小程序等）
- 🎯 TypeScript 类型支持
- ⚡ 良好的性能表现

