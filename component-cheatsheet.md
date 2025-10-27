# 图鸟UI Vue3 组件速查表

## 🎯 一分钟速查

### 基础组件

| 组件 | 用途 | 一行代码 |
|------|------|----------|
| TnButton | 按钮 | `<TnButton type="primary">按钮</TnButton>` |
| TnIcon | 图标 | `<TnIcon name="logo-tuniao" />` |
| TnTag | 标签 | `<TnTag type="primary">标签</TnTag>` |
| TnAvatar | 头像 | `<TnAvatar url="..." />` |
| TnBadge | 徽标 | `<TnBadge value="99" />` |

### 表单组件

| 组件 | 用途 | 一行代码 |
|------|------|----------|
| TnInput | 输入框 | `<TnInput v-model="value" placeholder="请输入" />` |
| TnCheckbox | 复选框 | `<TnCheckbox v-model="checked">选项</TnCheckbox>` |
| TnRadio | 单选框 | `<TnRadio v-model="value" label="1">选项</TnRadio>` |
| TnSwitch | 开关 | `<TnSwitch v-model="checked" />` |
| TnSlider | 滑动条 | `<TnSlider v-model="value" />` |
| TnNumberBox | 步进器 | `<TnNumberBox v-model="count" />` |
| TnRate | 评分 | `<TnRate v-model="score" />` |
| TnSearchBox | 搜索框 | `<TnSearchBox v-model="keyword" />` |

### 选择器

| 组件 | 用途 | 快速用法 |
|------|------|----------|
| TnPicker | 选择器 | `<TnPicker v-model="val" v-model:open="show" :data="[]" />` |
| TnDateTimePicker | 日期时间 | `<TnDateTimePicker v-model="date" mode="date" />` |
| TnRegionPicker | 地区选择 | `<TnRegionPicker v-model="region" />` |
| TnCalendar | 日历 | `<TnCalendar v-model="date" />` |

### 反馈组件

| 组件 | 用途 | 快速用法 |
|------|------|----------|
| TnModal | 模态框 | `modalRef.value?.showModal({content: '内容'})` |
| TnNotify | 消息通知 | `notifyRef.value?.show({msg: '成功'})` |
| TnActionSheet | 操作菜单 | `actionRef.value?.show({actions: []})` |
| TnPopup | 弹出框 | `<TnPopup v-model="show">内容</TnPopup>` |
| TnOverlay | 遮罩层 | `<TnOverlay v-model:show="show" />` |
| TnNoticeBar | 通知栏 | `<TnNoticeBar :data="['通知']" />` |

### 导航组件

| 组件 | 用途 | 快速用法 |
|------|------|----------|
| TnNavbar | 顶部导航 | `<TnNavbar fixed>标题</TnNavbar>` |
| TnTabbar | 底部导航 | `<TnTabbar v-model="cur"><TnTabbarItem /></TnTabbar>` |
| TnTabs | 标签栏 | `<TnTabs v-model="idx"><TnTabsItem /></TnTabs>` |

### 展示组件

| 组件 | 用途 | 快速用法 |
|------|------|----------|
| TnSwiper | 轮播图 | `<TnSwiper :data="imgs" width="100%" height="400" />` |
| TnProgress | 进度条 | `<TnLineProgress :percent="50" />` |
| TnLoading | 加载图标 | `<TnLoading show animation />` |
| TnLoadmore | 加载更多 | `<TnLoadmore status="loading" />` |
| TnEmpty | 空状态 | `<TnEmpty mode="data" />` |
| TnTitle | 标题 | `<TnTitle title="标题" mode="vLine" />` |
| TnSteps | 步骤条 | `<TnSteps v-model="step"><TnStepsItem /></TnSteps>` |

---

## 🎨 样式速查

### 颜色类
```vue
<!-- 背景色 -->
<view class="tn-blue_bg">蓝色背景</view>
<view class="tn-red_bg">红色背景</view>
<view class="tn-white_bg">白色背景</view>

<!-- 文字色 -->
<view class="tn-blue_text">蓝色文字</view>
<view class="tn-gray_text">灰色文字</view>
```

### 间距类
```vue
<!-- 内边距 -->
<view class="tn-p">默认内边距</view>
<view class="tn-p-sm">小内边距</view>
<view class="tn-p-lg">大内边距</view>
<view class="tn-pt">上内边距</view>

<!-- 外边距 -->
<view class="tn-m">默认外边距</view>
<view class="tn-mt">上外边距</view>
<view class="tn-mb-lg">大下外边距</view>
```

### 布局类
```vue
<!-- Flex布局 -->
<view class="tn-flex">Flex容器</view>
<view class="tn-flex-center">完全居中</view>
<view class="tn-flex-column">纵向布局</view>
<view class="tn-flex-1">占满剩余空间</view>
```

### 边框类
```vue
<view class="tn-border">边框</view>
<view class="tn-border-bottom">下边框</view>
<view class="tn-radius">圆角</view>
<view class="tn-radius-circle">圆形</view>
```

### 阴影类
```vue
<view class="tn-shadow">默认阴影</view>
<view class="tn-shadow-lg">大阴影</view>
```

---

## 📱 常用布局模式

### 卡片
```vue
<view class="tn-white_bg tn-radius tn-shadow tn-p">
  卡片内容
</view>
```

### 列表项
```vue
<view class="tn-white_bg tn-p tn-border-bottom">
  <view class="tn-flex tn-align-center">
    <view class="tn-flex-1">标题</view>
    <TnIcon name="right" />
  </view>
</view>
```

### 居中容器
```vue
<view class="tn-flex-center">
  完全居中的内容
</view>
```

### 底部固定按钮
```vue
<view class="fixed-bottom tn-white_bg tn-p">
  <TnButton type="primary" width="100%">确定</TnButton>
</view>

<style>
.fixed-bottom {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
}
</style>
```

---

## 🔤 主题色速查

### type属性值
- `primary` - 主题色（蓝色）
- `success` - 成功色（绿色）
- `warning` - 警告色（橙色）
- `danger` - 危险色（红色）
- `info` - 信息色（灰色）

### 使用示例
```vue
<TnButton type="primary">主题色</TnButton>
<TnButton type="success">成功色</TnButton>
<TnButton type="warning">警告色</TnButton>
<TnButton type="danger">危险色</TnButton>
<TnButton type="info">信息色</TnButton>

<TnTag type="primary">主题色标签</TnTag>
<TnBadge value="99" type="danger" />
<TnIcon name="star" type="warning" />
```

---

## 📏 尺寸速查

### size属性值
- `sm` - 小尺寸
- 默认 - 标准尺寸
- `lg` - 大尺寸
- `xl` - 超大尺寸

### 使用示例
```vue
<TnButton size="sm">小按钮</TnButton>
<TnButton>默认按钮</TnButton>
<TnButton size="lg">大按钮</TnButton>
<TnButton size="xl">超大按钮</TnButton>

<TnIcon name="star" size="20" />
<TnInput size="lg" />
<TnTag size="sm">小标签</TnTag>
```

---

## 🎭 形状速查

### shape属性值
- `circle` - 圆形
- `round` - 圆角
- `square` - 方形

### 使用示例
```vue
<TnButton shape="circle">圆形按钮</TnButton>
<TnButton shape="round">圆角按钮</TnButton>

<TnAvatar shape="circle" />
<TnAvatar shape="square" />

<TnTag shape="circle">圆形标签</TnTag>
<TnTag shape="round">圆角标签</TnTag>
```

---

## 🎪 组件Ref方法速查

### TnModal
```typescript
const modalRef = ref<TnModalInstance>()

// 显示模态框
modalRef.value?.showModal({ content: '内容' })
```

### TnNotify
```typescript
const notifyRef = ref<TnNotifyInstance>()

// 显示通知
notifyRef.value?.show({ msg: '消息' })
```

### TnActionSheet
```typescript
const actionRef = ref<TnActionSheetInstance>()

// 显示操作菜单
actionRef.value?.show({ actions: [] })
```

### TnForm
```typescript
const formRef = ref<TnFormInstance>()

// 验证表单
formRef.value?.validate((valid) => {})

// 验证指定字段
formRef.value?.validateField('username')

// 重置表单
formRef.value?.resetFields()

// 清除验证
formRef.value?.clearValidate()
```

### TnImageUpload
```typescript
const uploadRef = ref<TnImageUploadInstance>()

// 手动选择文件
uploadRef.value?.chooseFile()

// 手动上传
uploadRef.value?.upload()

// 重试失败文件
uploadRef.value?.retry()

// 清空文件
uploadRef.value?.clear()
```

### TnPicker
```typescript
const pickerRef = ref<TnPickerInstance>()

// 重置选择器
pickerRef.value?.resetPickerViewIndex()

// 重置指定范围
pickerRef.value?.resetPickerIndexWithPosition(0, 2)
```

### TnWaterFall
```typescript
const waterfallRef = ref<TnWaterFallInstance>()

// 重置瀑布流
waterfallRef.value?.reset()
```

### TnReadMore
```typescript
const readMoreRef = ref<TnReadMoreInstance>()

// 重置内容高度
readMoreRef.value?.resetContentHeight()
```

### TnCountDown
```typescript
const countDownRef = ref<TnCountDownInstance>()

// 开始倒计时
countDownRef.value?.start()

// 停止倒计时
countDownRef.value?.stop()

// 重置倒计时
countDownRef.value?.reset()
```

---

## 🎨 渐变色速查

### gradient__开头的渐变色
```vue
<TnButton bg-color="gradient__cool-1">渐变1</TnButton>
<TnButton bg-color="gradient__cool-2">渐变2</TnButton>
<TnButton bg-color="gradient__cool-3">渐变3</TnButton>
<TnButton bg-color="gradient__cool-4">渐变4</TnButton>
<TnButton bg-color="gradient__cool-5">渐变5</TnButton>
<TnButton bg-color="gradient__cool-6">渐变6</TnButton>
<TnButton bg-color="gradient__teal">青色渐变</TnButton>
```

---

## 📐 单位速查

### 支持的单位类型
- `rpx` - 响应式像素（默认单位）
- `px` - 像素
- `%` - 百分比
- `vh/vw` - 视口单位
- `em/rem` - 相对单位

### 使用示例
```vue
<!-- 默认rpx -->
<TnButton width="200" height="80">按钮</TnButton>

<!-- 指定单位 -->
<TnButton width="200rpx">rpx单位</TnButton>
<TnButton width="100px">px单位</TnButton>
<TnButton width="50%">百分比</TnButton>
<TnButton width="10vw">视口宽度</TnButton>
```

---

## 🎯 Props速查

### 通用Props（大多数组件支持）

| 属性 | 说明 | 类型 | 示例 |
|------|------|------|------|
| size | 尺寸 | String | `sm` / `lg` / `xl` |
| disabled | 禁用 | Boolean | `true` / `false` |
| custom-style | 自定义样式 | Object | `{ fontSize: '32rpx' }` |
| custom-class | 自定义类名 | String | `my-class` |

### 颜色相关Props

| 属性 | 说明 | 可用组件 | 示例值 |
|------|------|----------|--------|
| type | 主题色类型 | Button, Tag, Icon等 | `primary` / `success` / `warning` / `danger` / `info` |
| bg-color | 背景颜色 | Button, Tag, Avatar等 | `tn-blue` / `#01beff` / `gradient__cool-1` |
| text-color | 文字颜色 | Button, Tag等 | `tn-white` / `#ffffff` |
| color | 颜色（通用） | Icon, Title等 | `tn-blue` / `#01beff` |
| border-color | 边框颜色 | Button, Tag等 | `tn-grey` / `#e0e0e0` |

### 尺寸相关Props

| 属性 | 说明 | 可用组件 | 示例值 |
|------|------|----------|--------|
| width | 宽度 | Button, Input等 | `200` / `100%` / `200rpx` |
| height | 高度 | Button, Input等 | `80` / `80rpx` / `80px` |
| size | 预设尺寸 | 大多数组件 | `sm` / `lg` / `xl` |
| font-size | 字体大小 | Button, Tag等 | `28` / `28rpx` |

---

## 🔄 v-model绑定速查

### 单值绑定
```vue
<TnInput v-model="text" />
<TnSwitch v-model="checked" />
<TnSlider v-model="value" />
<TnRate v-model="score" />
```

### 数组绑定
```vue
<TnCheckboxGroup v-model="checkedList" />
<TnCalendar v-model="dateList" mode="multi" />
```

### 多个v-model
```vue
<!-- Popup -->
<TnPopup v-model="show">内容</TnPopup>

<!-- Picker -->
<TnPicker v-model="value" v-model:open="show" />

<!-- DateTimePicker -->
<TnDateTimePicker v-model="date" v-model:open="show" />

<!-- Keyboard -->
<TnKeyboard v-model="value" v-model:show="show" v-model:car-lang="lang" />

<!-- Overlay -->
<TnOverlay v-model:show="show" />
```

---

## 🎪 插槽速查

### 常用插槽

| 组件 | 插槽名 | 说明 |
|------|--------|------|
| TnButton | default | 按钮内容 |
| TnInput | prefix / suffix | 输入框前/后内容 |
| TnPopup | default / closeBtn | 弹窗内容 / 关闭按钮 |
| TnModal | default | 模态框内容 |
| TnActionSheet | title / cancel | 标题 / 取消按钮 |
| TnNavbar | default / back / right | 导航内容 / 返回区域 / 右侧区域 |
| TnForm | default | 表单项 |
| TnFormItem | default / label | 表单内容 / 标签 |
| TnSwiper | default | 轮播项内容 |
| TnAvatar | default | 头像内容 |
| TnBadge | default | 徽标附着的内容 |
| TnCollapse | default | 折叠项 |
| TnCollapseItem | default / title | 折叠内容 / 标题 |

### 插槽使用示例
```vue
<!-- 默认插槽 -->
<TnButton>按钮文字</TnButton>

<!-- 具名插槽 -->
<TnInput v-model="value">
  <template #prefix>
    <TnIcon name="user" />
  </template>
  <template #suffix>
    <TnButton size="sm">发送</TnButton>
  </template>
</TnInput>

<!-- 作用域插槽 -->
<TnSwiper :data="images">
  <template #default="{ data, active, index }">
    <image :src="data" mode="aspectFill" />
  </template>
</TnSwiper>
```

---

## 🎯 事件速查

### 常用事件

| 事件名 | 触发时机 | 可用组件 | 回调参数 |
|--------|----------|----------|----------|
| click | 点击时 | Button, Icon, Tag等 | - |
| change | 值改变时 | Input, Switch, Checkbox等 | value |
| input | 输入时 | Input, SearchBox | value |
| confirm | 确认时 | Picker, DateTimePicker, Keyboard | value |
| cancel | 取消时 | Picker, DateTimePicker等 | - |
| focus | 聚焦时 | Input | event |
| blur | 失焦时 | Input | event |
| clear | 清除时 | Input, SearchBox | - |
| search | 搜索时 | SearchBox | value |
| open | 打开时 | Popup, SwipeAction | - |
| close | 关闭时 | Popup, Picker等 | - |

### 事件使用示例
```vue
<!-- 基础事件 -->
<TnButton @click="handleClick">点击</TnButton>

<!-- 值改变事件 -->
<TnInput v-model="value" @change="handleChange" />

<!-- 多个事件 -->
<TnInput
  v-model="value"
  @input="handleInput"
  @change="handleChange"
  @focus="handleFocus"
  @blur="handleBlur"
  @clear="handleClear"
/>

<!-- 自定义事件参数 -->
<TnTabs @change="(index) => console.log('当前索引:', index)" />
```

---

## 🎨 颜色值格式速查

### 支持的颜色格式

```vue
<!-- 1. 内置颜色变量 -->
<TnButton bg-color="tn-blue">蓝色</TnButton>
<TnButton text-color="tn-red">红色文字</TnButton>

<!-- 2. 主题色 -->
<TnButton type="primary">主题色</TnButton>

<!-- 3. 渐变色 -->
<TnButton bg-color="gradient__cool-1">渐变色</TnButton>

<!-- 4. Hex颜色 -->
<TnButton bg-color="#01beff">蓝色</TnButton>

<!-- 5. RGB颜色 -->
<TnButton bg-color="rgb(1, 190, 255)">蓝色</TnButton>

<!-- 6. RGBA颜色 -->
<TnButton bg-color="rgba(1, 190, 255, 0.5)">半透明蓝色</TnButton>
```

---

## 🔧 表单验证规则速查

### 内置验证规则
```typescript
const rules = {
  // 必填
  username: [
    { required: true, message: '请输入用户名', trigger: 'blur' }
  ],
  
  // 长度限制
  password: [
    { min: 6, max: 16, message: '长度6-16个字符', trigger: 'blur' }
  ],
  
  // 正则验证
  phone: [
    { pattern: /^1[3-9]\d{9}$/, message: '手机号格式不正确', trigger: 'blur' }
  ],
  
  // 自定义验证
  age: [
    { 
      validator: (rule, value, callback) => {
        if (value < 18) {
          callback(new Error('年龄必须大于18岁'))
        } else {
          callback()
        }
      }, 
      trigger: 'change' 
    }
  ]
}
```

### trigger值
- `change` - 值改变时验证
- `blur` - 失焦时验证
- `['change', 'blur']` - 两种情况都验证

---

## 📊 数据格式速查

### Picker数据格式
```typescript
// 单列选择器 - 字符串数组
const data1 = ['选项1', '选项2', '选项3']

// 单列选择器 - 对象数组
const data2 = [
  { label: '选项1', value: 1 },
  { label: '选项2', value: 2 }
]

// 多列选择器
const data3 = [
  ['选项1-1', '选项1-2'],
  ['选项2-1', '选项2-2']
]

// 级联选择器
const data4 = [
  {
    label: '一级',
    value: 1,
    children: [
      { label: '二级1', value: 11 },
      { label: '二级2', value: 12 }
    ]
  }
]
```

### SwipeAction选项格式
```typescript
const options = [
  {
    text: '置顶',
    icon: 'star',
    bgColor: 'tn-orange',
    disabled: false,
    round: false
  }
]
```

### IndexList数据格式
```typescript
const data = {
  a: {
    title: 'A',
    data: [
      { id: 1, name: '张三', star: true }
    ]
  },
  b: {
    title: 'B',
    data: [
      { id: 2, name: '李四' }
    ]
  }
}
```

---

## 🚨 注意事项

### ⚠️ 微信小程序
- 使用`custom-class`和`custom-style`设置样式
- 某些CSS特性不支持（如backdrop-filter）

### ⚠️ 表单组件
- 必须在`TnFormItem`中设置`prop`属性
- `validate-event`控制是否触发表单验证

### ⚠️ 弹窗组件
- 需要通过ref调用方法显示（Modal, Notify, ActionSheet）
- 通过v-model控制显示（Popup）

### ⚠️ 图片组件
- 懒加载必须设置高度或使用`mode="widthFix"`
- 图片路径需要使用绝对路径或网络地址

### ⚠️ 颜色使用
- Switch, Slider等组件不支持渐变色
- 毛玻璃效果下只能使用rgba颜色

---

## 🔍 常见需求快速定位

**我想要...**

| 需求 | 使用组件 | 关键代码 |
|------|----------|----------|
| 显示确认对话框 | TnModal | `modalRef.value?.showModal({content: '...'})` |
| 底部弹出菜单 | TnActionSheet | `actionRef.value?.show({actions: []})` |
| 顶部消息提示 | TnNotify | `notifyRef.value?.show({msg: '...'})` |
| 从底部弹出内容 | TnPopup | `<TnPopup v-model="show" open-direction="bottom">` |
| 表单输入和验证 | TnForm + TnInput | 设置rules，调用validate |
| 选择日期 | TnCalendar | `<TnCalendar v-model="date" mode="date" />` |
| 选择地区 | TnRegionPicker | `<TnRegionPicker v-model="region" />` |
| 上传图片 | TnImageUpload | `<TnImageUpload v-model="imgs" :action="url" />` |
| 轮播图 | TnSwiper | `<TnSwiper :data="imgs" autoplay loop />` |
| 底部导航 | TnTabbar | `<TnTabbar v-model="cur"><TnTabbarItem /></TnTabbar>` |
| 标签页切换 | TnTabs | `<TnTabs v-model="idx"><TnTabsItem /></TnTabs>` |
| 显示加载中 | TnLoading | `<TnLoading show animation />` |
| 列表加载更多 | TnLoadmore | `<TnLoadmore status="loading" />` |
| 空数据提示 | TnEmpty | `<TnEmpty mode="data" />` |
| 商品数量选择 | TnNumberBox | `<TnNumberBox v-model="count" />` |
| 左滑删除 | TnSwipeAction | `<TnSwipeAction><TnSwipeActionItem /></TnSwipeAction>` |
| 步骤流程 | TnSteps | `<TnSteps v-model="step"><TnStepsItem /></TnSteps>` |
| 折叠面板 | TnCollapse | `<TnCollapse><TnCollapseItem /></TnCollapse>` |
| 评分 | TnRate | `<TnRate v-model="score" />` |
| 搜索 | TnSearchBox | `<TnSearchBox v-model="keyword" @search="..." />` |

---

## 🎨 常用颜色变量

### 背景色类名
```
tn-white_bg, tn-black_bg
tn-blue_bg, tn-blue-light_bg, tn-blue-dark_bg
tn-red_bg, tn-red-light_bg, tn-red-dark_bg
tn-green_bg, tn-green-light_bg, tn-green-dark_bg
tn-yellow_bg, tn-orange_bg, tn-purple_bg
tn-grey_bg, tn-grey-light_bg, tn-grey-dark_bg
```

### 文字颜色类名
```
tn-white_text, tn-black_text
tn-blue_text, tn-red_text, tn-green_text
tn-gray_text, tn-grey-disabled_text
tn-color-primary, tn-color-success
tn-color-warning, tn-color-danger, tn-color-info
```

---

## 📝 组件导入速查

### 单个组件导入
```typescript
// Node方式
import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'
import TnIcon from '@tuniao/tnui-vue3-uniapp/components/icon/src/icon.vue'
import TnInput from '@tuniao/tnui-vue3-uniapp/components/input/src/input.vue'

// uni_modules方式
import TnButton from '@/uni_modules/tuniaoui-vue3/components/button/src/button.vue'
import TnIcon from '@/uni_modules/tuniaoui-vue3/components/icon/src/icon.vue'
import TnInput from '@/uni_modules/tuniaoui-vue3/components/input/src/input.vue'
```

### 类型导入
```typescript
// Node方式
import type {
  TnModalInstance,
  TnFormInstance,
  FormRules,
  LoadmoreStatus,
} from '@tuniao/tnui-vue3-uniapp'

// uni_modules方式
import type {
  TnModalInstance,
  TnFormInstance,
  FormRules,
  LoadmoreStatus,
} from '@/uni_modules/tuniaoui-vue3'
```

---

## 🎯 完整示例索引

在 `quick-reference.md` 文件中可以找到以下完整示例：
1. ✅ 完整表单页面
2. ✅ 底部弹出选择器
3. ✅ 图片上传功能
4. ✅ 轮播图展示
5. ✅ 列表加载更多
6. ✅ 瀑布流布局
7. ✅ 底部导航栏
8. ✅ 自定义顶部导航

---

## 📚 推荐阅读顺序

### 第一天：基础入门
1. README.md - 了解知识库结构
2. tuniao-ui-knowledge-base.md - 浏览所有组件
3. component-cheatsheet.md（本文） - 快速查询

### 第二天：样式系统
1. style-system.md - 学习完整样式系统
2. 实践：使用内置样式类构建页面

### 第三天：组件实战
1. quick-reference.md - 学习常用代码片段
2. components-detail.md - 深入学习具体组件
3. 实践：构建实际页面

---

## 🎁 额外资源

### 在线工具
- [uni-app官方文档](https://uniapp.dcloud.io)
- [Vue3官方文档](https://cn.vuejs.org)
- [TypeScript官方文档](https://www.typescriptlang.org)

### 社区资源
- 图鸟UI官方社区
- uni-app开发者社区
- Vue3技术社区

---

**提示**：建议将本速查表加入浏览器书签或打印出来，方便随时查阅！ 🎉

