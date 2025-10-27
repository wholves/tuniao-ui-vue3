# 图鸟UI Vue3 组件库知识库

> 数据来源: https://vue3.tuniaokj.com
> 爬取时间: 2025-10-27
> 组件总数: 56个

## 目录

### 基础组件
- [按钮 Button](#button)
- [图标 Icon](#icon)
- [标签 Tag](#tag)
- [头像 Avatar](#avatar)
- [徽标 Badge](#badge)

### 表单组件
- [输入框 Input](#input)
- [复选框 Checkbox](#checkbox)
- [单选框 Radio](#radio)
- [开关 Switch](#switch)
- [步进器 NumberBox](#numberbox)
- [滑动条 Slider](#slider)
- [评分 Rate](#rate)
- [表单 Form](#form)
- [选择器 Picker](#picker)
- [日期时间选择器 DateTimePicker](#datetimepicker)
- [地区选择器 RegionPicker](#regionpicker)
- [搜索框 SearchBox](#searchbox)
- [软键盘 Keyboard](#keyboard)
- [图片上传 ImageUpload](#imageupload)

### 展示组件
- [轮播图 Swiper](#swiper)
- [标题 Title](#title)
- [进度条 Progress](#progress)
- [标签栏 Tabs](#tabs)
- [步骤条 Steps](#steps)
- [空白页 Empty](#empty)
- [加载更多 Loadmore](#loadmore)
- [加载图标 Loading](#loading)
- [倒计时 CountDown](#countdown)
- [数字跳转 CountTo](#countto)
- [数字滚动 CountScroll](#countscroll)
- [懒加载 LazyLoad](#lazyload)
- [相册 PhotoAlbum](#photoalbum)
- [瀑布流 WaterFall](#waterfall)

### 导航组件
- [顶部导航栏 Navbar](#navbar)
- [底部导航栏 Tabbar](#tabbar)

### 反馈组件
- [模态框 Modal](#modal)
- [操作菜单 ActionSheet](#actionsheet)
- [弹出框 Popup](#popup)
- [消息通知 Notify](#notify)
- [通知栏 NoticeBar](#noticebar)
- [遮罩层 Overlay](#overlay)

### 布局组件
- [列表 List](#list)
- [吸顶 Sticky](#sticky)
- [折叠面板 Collapse](#collapse)
- [滑动菜单 SwipeAction](#swipeaction)
- [分段器 Subsection](#subsection)
- [选项卡切换 SwitchTab](#switchtab)
- [气泡弹框 BubbleBox](#bubblebox)
- [横向滚动 ScrollList](#scrolllist)
- [索引列表 IndexList](#indexlist)
- [阅读更多 ReadMore](#readmore)

### 日历组件
- [日历 Calendar](#calendar)
- [周日历 WeekCalendar](#weekcalendar)

### 页面组件
- [页脚 Footer](#footer)

---

<a name="button"></a>
## TnButton - 按钮

### 组件说明
该组件内部实现以 uni-app 的 `button` 组件为基础，对其进行了扩展，使其能够在 uni-app 的各个平台上表现一致。

### 组件位置
- node方式: `import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'`
- uni_modules方式: `import TnButton from '@/uni_modules/tuniaoui-vue3/components/button/src/button.vue'`

### 基本用法
```vue
<TnButton>按钮</TnButton>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| width | 按钮宽度 | String \| Number | - | - |
| height | 按钮高度 | String \| Number | - | - |
| size | 按钮尺寸 | String | - | `sm` / `lg` / `xl` |
| shape | 按钮形状 | String | - | `circle` / `round` |
| type | 按钮颜色类型 | String | primary | `primary` / `success` / `warning` / `danger` / `info` |
| text | 文本按钮 | Boolean | false | true |
| plain | 朴素按钮 | Boolean | false | true |
| icon | 按钮图标 | String | - | - |
| bold | 字体加粗 | Boolean | false | true |
| font-size | 字体大小 | String | - | - |
| bg-color | 背景颜色 | String | - | - |
| text-color | 文字颜色 | String | - | - |
| border-bold | 边框加粗 | Boolean | false | true |
| border-color | 边框颜色 | String | - | - |
| shadow | 显示阴影 | Boolean | false | true |
| shadow-color | 阴影颜色 | String | - | - |
| disabled | 禁用 | Boolean | false | true |
| loading | 加载状态 | Boolean | false | true |

### 样式示例
```vue
<!-- 不同类型的按钮 -->
<TnButton type="primary">按钮</TnButton>
<TnButton type="success">按钮</TnButton>
<TnButton type="warning">按钮</TnButton>
<TnButton type="danger">按钮</TnButton>
<TnButton type="info">按钮</TnButton>

<!-- 不同形状的按钮 -->
<TnButton type="primary" shape="circle">按钮</TnButton>
<TnButton type="primary" shape="round">按钮</TnButton>

<!-- 不同尺寸的按钮 -->
<TnButton size="sm">按钮</TnButton>
<TnButton size="lg">按钮</TnButton>
<TnButton size="xl">按钮</TnButton>

<!-- 自定义颜色 -->
<TnButton bg-color="tn-blue">按钮</TnButton>
<TnButton bg-color="gradient__cool-1">按钮</TnButton>
<TnButton bg-color="#01beff">按钮</TnButton>
```

---

<a name="icon"></a>
## TnIcon - 图标

### 组件说明
基于字体的图标集，图鸟将所有图标进行了统一化，重绘了大多数的常见图标。

### 组件位置
- node方式: `import TnIcon from '@tuniao/tnui-vue3-uniapp/components/icon/src/icon.vue'`
- uni_modules方式: `import TnIcon from '@/uni_modules/tuniaoui-vue3/components/icon/src/icon.vue'`

### 基本用法
```vue
<TnIcon name="logo-tuniao" />
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| name | 图标名称 | String | - | - |
| type | 图标颜色类型 | String | - | `primary` / `success` / `warning` / `danger` / `info` |
| color | 图标颜色 | String | - | - |
| size | 图标尺寸大小 | String \| Number | - | - |
| bold | 加粗图标 | Boolean | false | true |
| transparent | 透明图标 | Boolean | false | true |
| transparent-bg | 透明图标背景色 | String | - | - |
| img-mode | 图片模式 | String | aspectFit | - |
| offset-top | 垂直偏移量 | String \| Number | - | - |

### 样式示例
```vue
<!-- 不同类型的图标 -->
<TnIcon name="logo-tuniao" type="primary" />
<TnIcon name="logo-tuniao" type="success" />
<TnIcon name="logo-tuniao" type="danger" />

<!-- 不同颜色的图标 -->
<TnIcon name="logo-tuniao" color="tn-blue" />
<TnIcon name="logo-tuniao" color="#01beff" />

<!-- 不同大小的图标 -->
<TnIcon name="logo-tuniao" size="20" />
<TnIcon name="logo-tuniao" size="20px" />

<!-- 透明图标 -->
<TnIcon name="logo-tuniao" transparent transparent-bg="tn-green" />
<TnIcon name="logo-tuniao" transparent transparent-bg="gradient__cool-1" />
```

---

<a name="input"></a>
## TnInput - 输入框

### 组件说明
此组件用于输入文字，支持单行和多行文本输入，一般情况下应该在 `TnFormItem` 中配合使用。

### 组件位置
- node方式: `import TnInput from '@tuniao/tnui-vue3-uniapp/components/input/src/input.vue'`
- uni_modules方式: `import TnInput from '@/uni_modules/tuniaoui-vue3/components/input/src/input.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const inputValue = ref('')
</script>

<template>
  <TnInput v-model="inputValue" placeholder="请输入用户名" />
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | String \| Number | - | - |
| type | 输入框类型 | String | text | `number` / `idcard` / `digit` / `textarea` / `password` / `select` |
| disabled | 禁用 | Boolean | false | true |
| size | 尺寸 | String \| Number | - | `sm` / `lg` |
| height | 高度 | String \| Number | - | - |
| text-align | 文字对齐 | String | left | `right` |
| placeholder | 占位文本 | String | - | - |
| border | 显示边框 | Boolean | true | false |
| border-color | 边框颜色 | String | - | - |
| underline | 下划线边框 | Boolean | false | true |
| maxlength | 最大长度 | Number | -1 | - |
| clearable | 清除按钮 | Boolean | false | true |
| show-password | 密码显示按钮 | Boolean | true | false |

### 不同类型示例
```vue
<!-- 文本输入框 -->
<TnInput v-model="inputValue" placeholder="请输入用户名" />

<!-- 数字输入框 -->
<TnInput v-model="inputValue" type="number" placeholder="请输入数字" />

<!-- 密码输入框 -->
<TnInput v-model="password" type="password" placeholder="请输入密码" />

<!-- 文本域 -->
<TnInput v-model="inputValue" type="textarea" placeholder="请输入描述" />

<!-- 选择框 -->
<TnInput v-model="pickerValue" type="select" placeholder="请选择" @click="openPicker" />
```

---

<a name="form"></a>
## TnForm - 表单

### 组件说明
此组件一般用于表单场景，可以配置 Input 输入框、Radio 单选框、Checkbox 多选框等，进行表单验证等。

### 组件位置
- node方式: `import TnForm from '@tuniao/tnui-vue3-uniapp/components/form/src/form.vue'`
- uni_modules方式: `import TnForm from '@/uni_modules/tuniaoui-vue3/components/form/src/form.vue'`

### 基本用法
```vue
<script setup>
import { reactive, ref } from 'vue'

const formRef = ref()
const formData = reactive({
  username: '',
})

const formRules = {
  username: [
    { required: true, message: '请输入用户名', trigger: ['change', 'blur'] },
    { pattern: /^[\w-]{4,16}$/, message: '请输入4-16位英文、数字、下划线、横线', trigger: ['change', 'blur'] },
  ],
}

const submitForm = () => {
  formRef.value?.validate((valid) => {
    if (valid) {
      uni.showToast({ title: '提交成功' })
    }
  })
}
</script>

<template>
  <TnForm ref="formRef" :model="formData" :rules="formRules">
    <TnFormItem label="用户名" prop="username">
      <TnInput v-model="formData.username" />
    </TnFormItem>
  </TnForm>
  <TnButton size="lg" @click="submitForm">提交</TnButton>
</template>
```

### Form 主要属性

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model | 表单数据对象 | Object | - |
| rules | 表单校验规则 | Object \| Array | - |
| size | 组件尺寸 | String | - |
| disabled | 禁用所有组件 | Boolean | false |
| label-position | label位置 | String | right |
| label-width | label宽度 | String \| Number | - |
| show-message | 显示校验结果 | Boolean | true |

---

<a name="popup"></a>
## TnPopup - 弹出框

### 组件说明
Popup 弹出框一般用于展示弹窗、信息提示等内容，支持上、下、左、右和中部弹出。

### 组件位置
- node方式: `import TnPopup from '@tuniao/tnui-vue3-uniapp/components/popup/src/popup.vue'`
- uni_modules方式: `import TnPopup from '@/uni_modules/tuniaoui-vue3/components/popup/src/popup.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const showPopup = ref(false)
</script>

<template>
  <TnPopup v-model="showPopup">
    <view class="tn-p-lg">弹框内容</view>
  </TnPopup>
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 显示与隐藏 | Boolean | false | true |
| open-direction | 弹出方向 | String | center | `top` / `bottom` / `left` / `right` |
| width | 宽度 | String \| Number | - | - |
| height | 高度 | String \| Number | - | - |
| bg-color | 背景颜色 | String | #fff | - |
| radius | 圆角 | String \| Number | 15 | - |
| overlay | 显示遮罩 | Boolean | true | false |
| overlay-closeable | 点击遮罩关闭 | Boolean | true | false |
| close-btn | 显示关闭按钮 | Boolean | false | true |
| close-btn-position | 关闭按钮位置 | String | right-top | - |

### 不同方向示例
```vue
<!-- 从顶部弹出 -->
<TnPopup v-model="showPopup" open-direction="top">
  <view class="tn-p-lg">弹框内容</view>
</TnPopup>

<!-- 从底部弹出 -->
<TnPopup v-model="showPopup" open-direction="bottom">
  <view class="tn-p-lg">弹框内容</view>
</TnPopup>

<!-- 从左侧弹出 -->
<TnPopup v-model="showPopup" open-direction="left">
  <view class="tn-p-lg">弹框内容</view>
</TnPopup>

<!-- 从右侧弹出 -->
<TnPopup v-model="showPopup" open-direction="right">
  <view class="tn-p-lg">弹框内容</view>
</TnPopup>

<!-- 从中间弹出 -->
<TnPopup v-model="showPopup" open-direction="center">
  <view class="tn-p-lg">弹框内容</view>
</TnPopup>
```

---

<a name="modal"></a>
## TnModal - 模态框

### 组件说明
Modal 模态框一般用于弹出提示信息，让用户确认下一步的操作或者提示用户操作结果。

### 组件位置
- node方式: `import TnModal from '@tuniao/tnui-vue3-uniapp/components/modal/src/modal.vue'`
- uni_modules方式: `import TnModal from '@/uni_modules/tuniaoui-vue3/components/modal/src/modal.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const modalRef = ref()

const openModal = () => {
  modalRef.value?.showModal({
    title: '操作提示',
    content: 'Modal内容',
  })
}
</script>

<template>
  <TnButton @click="openModal">显示模态框</TnButton>
  <TnModal ref="modalRef" />
</template>
```

### showModal 函数配置项

| 属性名 | 说明 | 类型 | 必填 |
|--------|------|------|------|
| content | 内容 | String | 是 |
| title | 标题 | String | 否 |
| showCancel | 显示取消按钮 | Boolean | 否 |
| cancelText | 取消按钮文字 | String | 否 |
| confirmText | 确认按钮文字 | String | 否 |
| mask | 显示遮罩 | Boolean | 否 |
| maskClosable | 点击遮罩关闭 | Boolean | 否 |
| cancel | 取消回调 | Function | 否 |
| confirm | 确认回调 | Function | 否 |

---

<a name="notify"></a>
## TnNotify - 消息通知

### 组件说明
Notify 消息通知一般用于让用户知道操作结果。

### 组件位置
- node方式: `import TnNotify from '@tuniao/tnui-vue3-uniapp/components/notify/src/notify.vue'`
- uni_modules方式: `import TnNotify from '@/uni_modules/tuniaoui-vue3/components/notify/src/notify.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const notifyRef = ref()

const showNotify = () => {
  notifyRef.value?.show({
    msg: '操作成功',
  })
}
</script>

<template>
  <TnButton @click="showNotify">显示通知</TnButton>
  <TnNotify ref="notifyRef" />
</template>
```

### show 函数配置参数

| 属性名 | 说明 | 类型 | 必填 |
|--------|------|------|------|
| msg | 消息内容 | String | 是 |
| type | 消息类型 | String | 否 |
| position | 通知位置 | String | 否 |
| bgColor | 背景颜色 | String | 否 |
| textColor | 字体颜色 | String | 否 |
| duration | 自动关闭时间 | Number | 否 |

---

<a name="tabs"></a>
## TnTabs - 标签栏

### 组件说明
该组件，是一个 tabs 标签栏组件，在标签多的时候，可以配置为左右滑动。

### 组件位置
- node方式: `import TnTabs from '@tuniao/tnui-vue3-uniapp/components/tabs/src/tabs.vue'`
- uni_modules方式: `import TnTabs from '@/uni_modules/tuniaoui-vue3/components/tabs/src/tabs.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'

const currentTabIndex = ref(0)
const tabsData = [
  { text: '关注' },
  { text: '推荐' },
  { text: '热榜' },
  { text: '搞笑' },
  { text: '视频' },
]
</script>

<template>
  <TnTabs v-model="currentTabIndex">
    <TnTabsItem
      v-for="(item, index) in tabsData"
      :key="index"
      :title="item.text"
    />
  </TnTabs>
</template>
```

### Tabs 主要属性

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
| scroll | 可滚动 | Boolean | true | false |
| bar | 显示滑块 | Boolean | true | false |
| active-bold | 激活加粗 | Boolean | true | false |

---

<a name="swiper"></a>
## TnSwiper - 轮播图

### 组件说明
该组件用于展示轮播信息。

### 组件位置
- node方式: `import TnSwiper from '@tuniao/tnui-vue3-uniapp/components/swiper/src/swiper.vue'`
- uni_modules方式: `import TnSwiper from '@/uni_modules/tuniaoui-vue3/components/swiper/src/swiper.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'

const currentSwiperIndex = ref(0)
const swiperData = [
  'https://resource.tuniaokj.com/images/xiongjie/x14.jpg',
  'https://resource.tuniaokj.com/images/xiongjie/xiong-3d-2.jpg',
  'https://resource.tuniaokj.com/images/xiongjie/xiong-3d-new.jpg',
]
</script>

<template>
  <TnSwiper v-model="currentSwiperIndex" :data="swiperData" width="100%" height="420">
    <template #default="{ data }">
      <view class="swiper-data">
        <image class="image" :src="data" mode="aspectFill" />
      </view>
    </template>
  </TnSwiper>
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| v-model/model-value | 当前选中索引 | Number | 0 |
| data | 轮播数据 | Array | [] |
| width | 宽度 | String | - |
| height | 高度 | String | - |
| autoplay | 自动播放 | Boolean | false |
| interval | 自动播放间隔 | Number | 5000 |
| duration | 动画时长 | Number | 500 |
| loop | 循环播放 | Boolean | false |
| indicator | 显示指示器 | Boolean | false |
| indicator-type | 指示器类型 | String | dot |

---

<a name="navbar"></a>
## TnNavbar - 顶部导航栏

### 组件说明
该组件一般用于特殊需要自定义顶部导航栏的情况。

### 组件位置
- node方式: `import TnNavbar from '@tuniao/tnui-vue3-uniapp/components/navbar/src/navbar.vue'`
- uni_modules方式: `import TnNavbar from '@/uni_modules/tuniaoui-vue3/components/navbar/src/navbar.vue'`

### 基本用法
```vue
<template>
  <!-- 固定在顶部 -->
  <TnNavbar fixed>TuniaoUI</TnNavbar>
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| height | 导航栏高度 | String | - |
| bg-color | 背景颜色 | String | - |
| text-color | 文字颜色 | String | - |
| frosted | 毛玻璃效果 | Boolean | false |
| back-icon | 返回图标 | String | left |
| back-text | 返回文字 | String | - |
| home-icon | 首页图标 | String | home-capsule-fill |
| bottom-shadow | 底部阴影 | Boolean | true |
| fixed | 固定在顶部 | Boolean | false |

---

<a name="tabbar"></a>
## TnTabbar - 底部导航栏

### 组件说明
该组件一般用于自定义底部导航栏，使用自定义底部导航栏可以让页面更加酷炫。

### 组件位置
- node方式: `import TnTabbar from '@tuniao/tnui-vue3-uniapp/components/tabbar/src/tabbar.vue'`
- uni_modules方式: `import TnTabbar from '@/uni_modules/tuniaoui-vue3/components/tabbar/src/tabbar.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'

const currentTabbar = ref(0)
const tabbarData = [
  { name: '首页', icon: 'home', activeIcon: 'home-fill' },
  { name: '爱好', icon: 'like', activeIcon: 'like-fill' },
  { name: '积分', icon: 'shop', activeIcon: 'shop-fill' },
  { name: '我的', icon: 'my-circle', activeIcon: 'my-circle-fill' },
]
</script>

<template>
  <TnTabbar v-model="currentTabbar" fixed>
    <TnTabbarItem
      v-for="(item, index) in tabbarData"
      :key="index"
      :icon="item.icon"
      :active-icon="item.activeIcon"
      :text="item.name"
    />
  </TnTabbar>
</template>
```

### Tabbar 主要属性

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| v-model/model-value | 当前选中索引 | String \| Number | - |
| height | 导航栏高度 | String | - |
| bg-color | 背景颜色 | String | - |
| inactive-color | 未选中颜色 | String | - |
| active-color | 选中颜色 | String | - |
| icon-size | 图标大小 | String | - |
| font-size | 文字大小 | String | - |
| fixed | 固定在底部 | Boolean | false |

---

<a name="calendar"></a>
## TnCalendar - 日历

### 组件说明
此组件用于选择日期，可以选择单个日期、多个日期、日期区间。

### 组件位置
- node方式: `import TnCalendar from '@tuniao/tnui-vue3-uniapp/components/calendar/src/calendar.vue'`
- uni_modules方式: `import TnCalendar from '@/uni_modules/tuniaoui-vue3/components/calendar/src/calendar.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const selectDate = ref('')
</script>

<template>
  <TnCalendar v-model="selectDate" />
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定日期值 | String \| Array | - | - |
| mode | 日历模式 | String | date | `multi` / `range` |
| min-date | 最小日期 | String \| Number | - | - |
| max-date | 最大日期 | String \| Number | - | - |
| active-bg-color | 选中背景色 | String | - | - |
| active-text-color | 选中文字色 | String | - | - |
| show-lunar | 显示农历 | Boolean | false | true |

### 不同模式示例
```vue
<!-- 单选模式 -->
<TnCalendar v-model="selectDate" mode="date" />

<!-- 多选模式 -->
<TnCalendar v-model="selectDate" mode="multi" />

<!-- 区间模式 -->
<TnCalendar v-model="selectDate" mode="range" />
```

---

<a name="picker"></a>
## TnPicker - 选择器

### 组件说明
Picker 选择器一般用于选择一项或者多项数据。

### 组件位置
- node方式: `import TnPicker from '@tuniao/tnui-vue3-uniapp/components/picker/src/picker.vue'`
- uni_modules方式: `import TnPicker from '@/uni_modules/tuniaoui-vue3/components/picker/src/picker.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'

const openPicker = ref(false)
const pickerValue = ref('数值2')
const pickerData = ['数值1', '数值2', '数值3', '数值4', '数值5']
</script>

<template>
  <TnPicker v-model="pickerValue" v-model:open="openPicker" :data="pickerData" />
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | Array \| String \| Number | - |
| open/v-model:open | 显示与隐藏 | Boolean | false |
| data | 选项数据 | Array | - |
| show-cancel | 显示取消按钮 | Boolean | true |
| cancel-text | 取消按钮文本 | String | 取消 |
| show-confirm | 显示确认按钮 | Boolean | true |
| confirm-text | 确认按钮文本 | String | 确定 |

---

<a name="progress"></a>
## TnProgress - 进度条

### 组件说明
Progress 进度条一般用于展示数据的场景，支持线形和圆形两种类型。

### 组件位置
- node方式: 
  - `import TnLineProgress from '@tuniao/tnui-vue3-uniapp/components/line-progress/src/line-progress.vue'`
  - `import TnCircleProgress from '@tuniao/tnui-vue3-uniapp/components/circle-progress/src/circle-progress.vue'`
- uni_modules方式:
  - `import TnLineProgress from '@/uni_modules/tuniaoui-vue3/components/line-progress/src/line-progress.vue'`
  - `import TnCircleProgress from '@/uni_modules/tuniaoui-vue3/components/circle-progress/src/circle-progress.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const progressPercent = ref(30)
</script>

<template>
  <!-- 线形进度条 -->
  <TnLineProgress :percent="progressPercent" />
  
  <!-- 圆形进度条 -->
  <TnCircleProgress :percent="progressPercent" />
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| percent | 进度值 | Number | 0 |
| active-color | 已完成颜色 | String | - |
| inactive-color | 未完成颜色 | String | - |
| show-percent | 显示进度值 | Boolean | false |
| duration | 动画时长(ms) | Number | 1500 |

---

<a name="loading"></a>
## TnLoading - 加载图标

### 组件说明
此组件是一个加载动画的图标。

### 组件位置
- node方式: `import TnLoading from '@tuniao/tnui-vue3-uniapp/components/loading/src/loading.vue'`
- uni_modules方式: `import TnLoading from '@/uni_modules/tuniaoui-vue3/components/loading/src/loading.vue'`

### 基本用法
```vue
<TnLoading show type="primary" />
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| show | 显示加载图标 | Boolean | false | true |
| animation | 显示动画 | Boolean | false | true |
| mode | 加载模式 | String | circle | `flower` / `semicircle` |
| type | 颜色类型 | String | primary | `success` / `warning` / `danger` / `info` |
| color | 颜色 | String | - | - |
| size | 大小 | String \| Number | - | `sm` / `lg` / `xl` |

---

<a name="checkbox"></a>
## TnCheckbox - 复选框

### 组件说明
复选框一般用于表示多个选项中的一个或多个状态。

### 组件位置
- node方式: `import TnCheckbox from '@tuniao/tnui-vue3-uniapp/components/checkbox/src/checkbox.vue'`
- uni_modules方式: `import TnCheckbox from '@/uni_modules/tuniaoui-vue3/components/checkbox/src/checkbox.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const selectValue = ref(['value1'])
</script>

<template>
  <TnCheckboxGroup v-model="selectValue">
    <TnCheckbox label="value1">value1</TnCheckbox>
    <TnCheckbox label="value2">value2</TnCheckbox>
  </TnCheckboxGroup>
</template>
```

### Checkbox 主要属性

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | String \| Number \| Boolean | - |
| label | 复选框的值 | String \| Number | - |
| size | 尺寸 | String | - |
| checked-shape | 选框形状 | String | square |
| disabled | 禁用 | Boolean | false |
| border | 显示边框 | Boolean | false |
| active-color | 选中颜色 | String | - |

---

<a name="radio"></a>
## TnRadio - 单选框

### 组件说明
单选框一般用于在多个备选项中进行单选，如性别选择等。

### 组件位置
- node方式: `import TnRadio from '@tuniao/tnui-vue3-uniapp/components/radio/src/radio.vue'`
- uni_modules方式: `import TnRadio from '@/uni_modules/tuniaoui-vue3/components/radio/src/radio.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const selectValue = ref('')
</script>

<template>
  <TnRadioGroup v-model="selectValue">
    <TnRadio label="男">男</TnRadio>
    <TnRadio label="女">女</TnRadio>
  </TnRadioGroup>
</template>
```

### Radio 主要属性

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| model-value/v-model | 绑定值 | String \| Number \| Boolean | - |
| label | 单选框的值 | String \| Number \| Boolean | - |
| size | 尺寸 | String | - |
| disabled | 禁用 | Boolean | false |
| border | 显示边框 | Boolean | false |
| active-color | 选中颜色 | String | - |

---

<a name="switch"></a>
## TnSwitch - 开关

### 组件说明
Switch 开关一般用于状态的打开和关闭之间进行切换。

### 组件位置
- node方式: `import TnSwitch from '@tuniao/tnui-vue3-uniapp/components/switch/src/switch.vue'`
- uni_modules方式: `import TnSwitch from '@/uni_modules/tuniaoui-vue3/components/switch/src/switch.vue'`

### 基本用法
```vue
<script setup>
import { ref } from 'vue'
const selectValue = ref(false)
</script>

<template>
  <TnSwitch v-model="selectValue" />
</template>
```

### 主要属性 (Props)

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| model-value/v-model | 绑定值 | String \| Number \| Boolean | - | - |
| shape | 形状 | String | round | `square` |
| size | 尺寸 | String | - | `sm` / `lg` |
| width | 宽度 | String \| Number | - | - |
| disabled | 禁用 | Boolean | false | true |
| loading | 加载状态 | Boolean | false | true |
| inactive-color | 未选中颜色 | String | - | - |
| active-color | 选中颜色 | String | - | - |
| inactive-text | 未选中文本 | String | - | - |
| active-text | 选中文本 | String | - | - |

---

## 图鸟UI 内置样式系统

### 颜色系统
图鸟UI内置了丰富的颜色系统，支持以下方式使用：
- 内置颜色变量：`tn-blue`、`tn-red`、`tn-green`、`tn-yellow`等
- 渐变色：`gradient__cool-1`、`gradient__cool-2`等
- 标准颜色：`hex`、`rgb`、`rgba`

### 尺寸系统
大多数组件支持以下尺寸：
- `sm` - 小尺寸
- 默认尺寸
- `lg` - 大尺寸
- `xl` - 超大尺寸

### 间距系统
- `tn-p` - 内边距
- `tn-m` - 外边距
- `tn-p-xs`、`tn-p-sm`、`tn-p-lg`、`tn-p-xl` - 不同大小的内边距
- `tn-mt`、`tn-mr`、`tn-mb`、`tn-ml` - 单边外边距

### Flex布局
- `tn-flex-center` - 居中对齐
- `tn-flex-column` - 纵向布局

---

## 完整组件列表及API


