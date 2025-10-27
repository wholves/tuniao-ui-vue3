# 图鸟UI Vue3 第三方组件文档

> 第三方组件是图鸟UI的扩展组件，通过npm安装使用  
> 📅 更新时间：2025-10-27

## 📦 第三方组件介绍

在TuniaoUI vue3版本中，图鸟推出了第三方组件的支持，开发者可以通过安装的方式去安装第三方的包，然后在TuniaoUI中使用。

第三方插件可以进一步的减少TuniaoUI的体积，同时也可以让开发者更加灵活的使用TuniaoUI。

### ⚠️ 注意事项

**第三方插件/组件暂时只支持以下方式创建的项目：**
- ✅ `tuniao-cli` 方式创建的项目
- ✅ 通过node方式安装TuniaoUI vue3的项目
- ❌ 其他方式创建的项目暂不支持

### 🤝 加入开发

如果你想开发第三方组件，可以联系微信: `tnkewo` (加微信时备注好tuniaoUI vue3 插件开发)。

---

## 📋 第三方组件列表

### 1. TnSuspendButton - 悬浮按钮

#### 组件说明
该组件一般用于将按钮悬浮在页面的指定位置，方便用户进行跳转等操作。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-suspend-button
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-suspend-button

#### 安装方式
```bash
# npm
npm i tnuiv3p-tn-suspend-button

# pnpm
pnpm add tnuiv3p-tn-suspend-button

# yarn
yarn add tnuiv3p-tn-suspend-button
```

#### 组件引入
```typescript
import TnSuspendButton from 'tnuiv3p-tn-suspend-button/index.vue'
```

#### 基本用法
```vue
<script setup>
import TnSuspendButton from 'tnuiv3p-tn-suspend-button/index.vue'
</script>

<template>
  <TnSuspendButton icon="logo-tuniao" />
</template>
```

#### Props

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| icon | 按钮显示的图标 | String | - | 图标有效值 |
| top | 距离顶部的距离 | String | 80% | - |
| right | 距离右边的距离 | String | 5% | - |
| bg-color | 背景颜色 | String | tn-type-primary | - |
| text-color | 文字颜色 | String | tn-color-white | - |
| size | 按钮尺寸 | String | - | `sm` / `lg` / `xl` |
| shape | 按钮形状 | String | circle | `square` |
| opacity | 透明度 | Number | 0.9 | - |
| shadow | 显示阴影 | Boolean | true | false |
| float | 漂浮动画 | Boolean | true | false |
| fixed | 固定定位 | Boolean | true | false |

#### Emits

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 按钮点击事件 | () => void |

#### 使用示例
```vue
<script setup>
import TnSuspendButton from 'tnuiv3p-tn-suspend-button/index.vue'
</script>

<template>
  <!-- 基础使用 -->
  <TnSuspendButton icon="logo-tuniao" />
  
  <!-- 自定义位置 -->
  <TnSuspendButton icon="logo-tuniao" top="90%" right="30" />
  
  <!-- 自定义样式 -->
  <TnSuspendButton 
    icon="logo-tuniao" 
    size="lg"
    bg-color="gradient__cool-6"
    text-color="#fff"
  />
  
  <!-- 方形按钮 -->
  <TnSuspendButton icon="logo-tuniao" shape="square" />
  
  <!-- 相对定位 -->
  <TnSuspendButton icon="logo-tuniao" :fixed="false" />
</template>
```

---

### 2. TnImageCrop - 图片裁剪

#### 组件说明
该组件一般用于图片裁剪场景。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-image-crop
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-image-crop

#### 安装方式
```bash
npm i tnuiv3p-tn-image-crop
```

#### 组件引入
```typescript
import TnImageCrop from 'tnuiv3p-tn-image-crop/index.vue'
```

#### 基本用法
```vue
<script setup>
import { ref } from 'vue'
import TnImageCrop from 'tnuiv3p-tn-image-crop/index.vue'

const image = 'https://resource.tuniaokj.com/images/content/rodion.jpg'
</script>

<template>
  <view class="content">
    <TnImageCrop :src="image" />
  </view>
</template>

<style>
.content {
  position: relative;
  width: 100%;
  height: 100vh;
}
</style>
```

#### Props

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| src | 图片地址 | String | - | - |
| circle | 圆形裁剪框 | Boolean | false | true |
| border-color | 裁剪框边框颜色 | String | #fff | - |
| bg-color | 容器背景颜色 | String | rgba(0, 0, 0, 0.5) | - |
| z-index | zIndex | Number | 100 | - |
| min-scale | 最小缩放系数 | Number | 0.5 | - |
| max-scale | 最大缩放系数 | Number | 2 | - |

#### Expose方法

| 函数名 | 说明 | 类型 |
|--------|------|------|
| save | 保存图片 | (options?) => Promise<string> |

#### GenerateImageOption

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| base64 | 返回base64格式 | boolean | false |
| cropRatio | 裁剪比例(0~1) | number | 1 |
| quality | 图片质量(0~1) | number | 1 |

#### 完整示例
```vue
<script setup>
import { ref } from 'vue'
import TnImageCrop from 'tnuiv3p-tn-image-crop/index.vue'
import type { TnImageCropInstance } from 'tnuiv3p-tn-image-crop'

const imageCropRef = ref<TnImageCropInstance>()
const image = 'https://resource.tuniaokj.com/images/content/rodion.jpg'

// 保存裁剪后的图片
const saveImage = async () => {
  const imageData = await imageCropRef.value?.save({
    base64: false,
    cropRatio: 1,
    quality: 0.8
  })
  console.log('裁剪后的图片:', imageData)
}
</script>

<template>
  <view class="content">
    <TnImageCrop ref="imageCropRef" :src="image" />
  </view>
  <view class="button">
    <TnButton size="xl" @click="saveImage">保存图片</TnButton>
  </view>
</template>
```

---

### 3. TnSignBoard - 签名板

#### 组件说明
该组件一般用于让用户填写签名。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-sign-board
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-sign-board

#### 安装方式
```bash
npm i tnuiv3p-tn-sign-board
```

#### 组件引入
```typescript
import TnSignBoard from 'tnuiv3p-tn-sign-board/index.vue'
```

#### 基本用法
```vue
<script setup>
import { ref } from 'vue'
import TnSignBoard from 'tnuiv3p-tn-sign-board/index.vue'
import type { TnSignBoardInstance } from 'tnuiv3p-tn-sign-board'

const signBoardRef = ref<TnSignBoardInstance>()
const imagePath = ref('')

// 保存签名
const saveSign = () => {
  signBoardRef.value?.save().then((res) => {
    imagePath.value = res
  })
}

// 清空签名
const clearSign = () => {
  signBoardRef.value?.clear()
}
</script>

<template>
  <view class="demo">
    <TnSignBoard ref="signBoardRef" />
  </view>
  <view class="tn-mt tn-flex-center">
    <TnButton @click="saveSign">保存</TnButton>
    <TnButton type="danger" @click="clearSign">重新签名</TnButton>
  </view>
</template>

<style>
.demo {
  position: relative;
  width: 100%;
  height: 460rpx;
  border: 1rpx solid var(--tn-color-gray-disabled);
}
</style>
```

#### Props

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| width | 签名板宽度 | String | 100% | - |
| height | 签名板高度 | String | 100% | - |
| text-color | 签名颜色 | String | #080808 | - |
| disabled | 禁用签名板 | Boolean | false | true |

#### Emits

| 事件名 | 说明 | 类型 |
|--------|------|------|
| touch-start | 触摸开始事件 | () => void |
| touch-end | 触摸结束事件 | () => void |

#### Methods

| 方法名 | 说明 | 类型 |
|--------|------|------|
| save | 保存签名 | (rotate?: boolean) => Promise<string> |
| clear | 清空签名板 | () => void |

---

### 4. TnColorSelect - 颜色选择器

#### 组件说明
该组件用于选择颜色。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-color-select
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-color-select

#### 安装方式
```bash
npm i tnuiv3p-tn-color-select
```

#### 组件引入
```typescript
import TnColorSelect from 'tnuiv3p-tn-color-select/index.vue'
```

#### 基本用法
```vue
<script setup>
import { ref } from 'vue'
import TnColorSelect from 'tnuiv3p-tn-color-select/index.vue'

const color = ref('')
</script>

<template>
  <TnColorSelect v-model="color" />
</template>
```

#### Props

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 选择颜色的值 | String | #FF0000 | - |
| size | 颜色预览框尺寸 | String | - | `sm` / `lg` / `xl` |
| disabled | 禁用 | Boolean | false | true |
| validate-event | 触发表单验证 | Boolean | true | false |

#### Emits

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 颜色改变 | (value: string) => void |

#### 使用示例
```vue
<script setup>
import { ref } from 'vue'
import TnColorSelect from 'tnuiv3p-tn-color-select/index.vue'

const color = ref('#FF0000')

const handleColorChange = (value) => {
  console.log('选择的颜色:', value)
}
</script>

<template>
  <!-- 不同尺寸 -->
  <TnColorSelect v-model="color" size="sm" @change="handleColorChange" />
  <TnColorSelect v-model="color" size="lg" />
  <TnColorSelect v-model="color" size="xl" />
  
  <!-- 自定义尺寸 -->
  <TnColorSelect v-model="color" size="120rpx" />
</template>
```

---

### 5. TnStackSwiper - 堆叠轮播

#### 组件说明
该组件一般用于多张堆叠在一起的轮播场景。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-stack-swiper
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-stack-swiper

#### 安装方式
```bash
npm i tnuiv3p-tn-stack-swiper
```

#### 组件引入
```typescript
import TnStackSwiper from 'tnuiv3p-tn-stack-swiper/index.vue'
import TnStackSwiperItem from 'tnuiv3p-tn-stack-swiper/item.vue'
```

#### 基本用法
```vue
<script setup>
import TnStackSwiper from 'tnuiv3p-tn-stack-swiper/index.vue'
import TnStackSwiperItem from 'tnuiv3p-tn-stack-swiper/item.vue'
</script>

<template>
  <view class="swiper">
    <TnStackSwiper>
      <TnStackSwiperItem>
        <view class="swiper-item tn-bluepurple_bg">1</view>
      </TnStackSwiperItem>
      <TnStackSwiperItem>
        <view class="swiper-item tn-aquablue_bg">2</view>
      </TnStackSwiperItem>
      <TnStackSwiperItem>
        <view class="swiper-item tn-blue_bg">3</view>
      </TnStackSwiperItem>
    </TnStackSwiper>
  </view>
</template>

<style>
.swiper {
  position: relative;
  width: 100%;
  height: 400rpx;
}
.swiper-item {
  width: 100%;
  height: 100%;
  border-radius: 16rpx;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 50rpx;
  color: #fff;
}
</style>
```

#### TnStackSwiper Props

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 当前激活的item索引 | Number | 0 | - |
| width | 容器宽度 | String | 100% | - |
| height | 容器高度 | String | 100% | - |
| autoplay | 自动切换 | Boolean | false | true |
| interval | 切换时间(ms) | Number | 5000 | - |
| switch-rate | 滑动切换比例(0~1) | Number | 0.13 | - |
| scale-rate | 缩放比例(0~1) | Number | 0.08 | - |
| opacity-rate | 透明度比例(0~1) | Number | 0.18 | - |
| slide-direction | 滑动方向 | String | horizontal | `vertical` |

#### Emits

| 事件名 | 说明 | 类型 |
|--------|------|------|
| change | 轮播切换 | (index: number) => void |
| click | 点击事件 | (index: number) => void |

#### 高级用法
```vue
<script setup>
import { ref } from 'vue'
import TnStackSwiper from 'tnuiv3p-tn-stack-swiper/index.vue'
import TnStackSwiperItem from 'tnuiv3p-tn-stack-swiper/item.vue'

const currentIndex = ref(0)

const handleChange = (index) => {
  console.log('当前索引:', index)
}
</script>

<template>
  <!-- 自定义宽高 -->
  <TnStackSwiper 
    v-model="currentIndex"
    width="80vw" 
    height="400"
    @change="handleChange"
  >
    <TnStackSwiperItem v-for="i in 5" :key="i">
      <view class="swiper-item">{{ i }}</view>
    </TnStackSwiperItem>
  </TnStackSwiper>
  
  <!-- 垂直方向 -->
  <TnStackSwiper slide-direction="vertical">
    <TnStackSwiperItem>
      <view class="swiper-item">内容</view>
    </TnStackSwiperItem>
  </TnStackSwiper>
  
  <!-- 自动播放 -->
  <TnStackSwiper autoplay :interval="3000">
    <TnStackSwiperItem>
      <view class="swiper-item">内容</view>
    </TnStackSwiperItem>
  </TnStackSwiper>
</template>
```

---

### 6. TnVerifyCodeInput - 验证码输入

#### 组件说明
该组件用于输入验证码的场景。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-verify-code-input
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-verify-code-input

#### 安装方式
```bash
npm i tnuiv3p-tn-verify-code-input
```

#### 组件引入
```typescript
import TnVerifyCodeInput from 'tnuiv3p-tn-verify-code-input/index.vue'
```

#### 基本用法
```vue
<script setup>
import { ref } from 'vue'
import TnVerifyCodeInput from 'tnuiv3p-tn-verify-code-input/index.vue'

const codeInput = ref('')
</script>

<template>
  <TnVerifyCodeInput v-model="codeInput" />
</template>
```

#### Props

| 属性名 | 说明 | 类型 | 默认值 | 可选值 |
|--------|------|------|--------|--------|
| v-model/model-value | 验证码的值 | String \| Number | - | - |
| length | 验证码长度 | Number | 4 | - |
| width | 每个输入框宽度 | String | - | - |
| focus | 自动聚焦 | Boolean | true | false |
| disabled | 禁用 | Boolean | false | true |
| breath | 呼吸灯效果 | Boolean | true | false |
| password | 密码输入 | Boolean | false | true |
| input-type | 输入框类型 | String | border | `border-vline` / `border-hline` / `middle-hline` / `middle-vline` / `bottom-hline` |
| inactive-color | 默认颜色 | String | - | - |
| active-color | 激活颜色 | String | - | - |
| validate-event | 触发表单验证 | Boolean | true | false |

#### Emits

| 事件名 | 说明 | 类型 |
|--------|------|------|
| input | 输入时触发 | (value: string \| number) => void |
| change | 值改变时触发 | (value: string \| number) => void |
| complete | 输入完成时触发 | () => void |

#### 不同类型示例
```vue
<script setup>
import { ref } from 'vue'
import TnVerifyCodeInput from 'tnuiv3p-tn-verify-code-input/index.vue'

const code = ref('')
</script>

<template>
  <!-- 边框类型(默认) -->
  <TnVerifyCodeInput v-model="code" input-type="border" />
  
  <!-- 边框带垂直竖线 -->
  <TnVerifyCodeInput v-model="code" input-type="border-vline" />
  
  <!-- 边框带居中横线 -->
  <TnVerifyCodeInput v-model="code" input-type="border-hline" />
  
  <!-- 垂直居中竖线 -->
  <TnVerifyCodeInput v-model="code" input-type="middle-vline" />
  
  <!-- 居中横线 -->
  <TnVerifyCodeInput v-model="code" input-type="middle-hline" />
  
  <!-- 底部横线 -->
  <TnVerifyCodeInput v-model="code" input-type="bottom-hline" />
  
  <!-- 6位验证码 -->
  <TnVerifyCodeInput v-model="code" :length="6" />
  
  <!-- 密码模式 -->
  <TnVerifyCodeInput v-model="code" password />
</template>
```

---

### 7. TnUpdateUserInfoPopup - 修改用户信息弹框

#### 组件说明
该组件一般用于更新用户的头像和昵称信息。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-update-user-info-popup
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-update-user-info-popup

#### 安装方式
```bash
npm i tnuiv3p-tn-update-user-info-popup
```

#### 组件引入
```typescript
import TnUpdateUserInfoPopup from 'tnuiv3p-tn-update-user-info-popup/index.vue'
```

#### 基本用法
```vue
<script setup>
import { ref } from 'vue'
import TnUpdateUserInfoPopup from 'tnuiv3p-tn-update-user-info-popup/index.vue'

const showPopup = ref(false)
const nickname = ref('')
const avatar = ref('')

// 头像选择事件
const avatarChooseHandle = (url) => {
  // 上传到服务器
  uni.uploadFile({
    url: '服务器地址',
    fileType: 'image',
    filePath: url,
    name: 'file',
    success: (res) => {
      const data = JSON.parse(res.data)
      avatar.value = data.data.url
    },
  })
}

// 确认事件
const confirmHandle = (avatarVal, nicknameVal) => {
  console.log('头像:', avatarVal)
  console.log('昵称:', nicknameVal)
  // 保存到服务器
}
</script>

<template>
  <TnButton @click="showPopup = true">修改用户信息</TnButton>
  
  <TnUpdateUserInfoPopup
    v-model:show="showPopup"
    v-model:nickname="nickname"
    v-model:avatar="avatar"
    @choose-avatar="avatarChooseHandle"
    @confirm="confirmHandle"
  />
</template>
```

#### Props

| 属性名 | 说明 | 类型 | 默认值 |
|--------|------|------|--------|
| show | 显示/隐藏 | Boolean | true |
| avatar | 用户头像地址 | String | - |
| nickname | 用户昵称 | String | - |
| title | 弹框标题 | String | 获取您的昵称、头像 |
| tips | 弹框提示 | String | - |
| confirm-text | 确认按钮文案 | String | 保存 |
| confirm-bg-color | 确认按钮背景色 | String | tn-type-primary |
| confirm-text-color | 确认按钮文字色 | String | tn-white |

#### Events

| 事件名 | 说明 | 类型 |
|--------|------|------|
| choose-avatar | 头像选择事件 | (url: string) => void |
| confirm | 确认按钮点击事件 | (avatar: string, nickname: string) => void |

#### ⚠️ 注意事项
- 在微信小程序模拟器中无法获取到用户的昵称，需要在真机上测试
- 头像上传需要用户处理 `choose-avatar` 事件，将头像上传到服务器

---

### 8. TnDropdown - 下拉框

#### 组件说明
该组件一般用于点击之后在下拉框中展示内容的场景。

#### 仓库地址
- GitHub: https://github.com/HighSpecific/tnuiv3p-dropdown
- npmjs: https://www.npmjs.com/package/tnuiv3p-tn-dropdown

#### 安装方式
```bash
npm i tnuiv3p-tn-dropdown
```

#### 组件引入
```typescript
import TnDropdown from 'tnuiv3p-tn-dropdown/index.vue'
```

#### 基本用法
```vue
<script setup>
import { ref } from 'vue'
import TnDropdown from 'tnuiv3p-tn-dropdown/index.vue'

const openDropdown = ref(false)

const menuItemClickHandle = () => {
  openDropdown.value = false
}
</script>

<template>
  <TnDropdown v-model:open="openDropdown">
    <template #menu>
      <view class="dropdown-menu">
        <view class="dropdown-menu-item" @tap.stop="menuItemClickHandle">
          选项一
        </view>
        <view class="dropdown-menu-item" @tap.stop="menuItemClickHandle">
          选项二
        </view>
        <view class="dropdown-menu-item" @tap.stop="menuItemClickHandle">
          选项三
        </view>
      </view>
    </template>
    <view class="dropdown-content">下拉内容</view>
  </TnDropdown>
</template>

<style>
.dropdown-menu {
  position: relative;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.dropdown-menu-item {
  flex: 1;
  background-color: var(--tn-color-gray-light);
  padding: 20rpx 0rpx;
  display: flex;
  align-items: center;
  justify-content: center;
}
.dropdown-content {
  position: relative;
  width: 100%;
  height: 500rpx;
  background-color: var(--tn-color-white);
}
</style>
```

#### Props

| 参数 | 说明 | 类型 | 默认值 | 可选值 |
|------|------|------|--------|--------|
| open/v-model:open | 下拉菜单打开状态 | Boolean | false | true |
| bg-color | 背景颜色 | String | #fff | - |
| height | 下拉框高度 | String | - | - |
| overlay | 显示遮罩 | Boolean | true | false |
| border-radius | 带圆角 | Boolean | true | false |
| shadow | 显示阴影 | Boolean | false | true |
| menu-content-gap | 菜单和内容间距 | String | - | - |
| z-index | zIndex | Number | 999 | - |

#### Events

| 事件名 | 说明 | 回调参数 |
|--------|------|----------|
| close | 下拉框关闭时触发 | - |

#### Slots

| 插槽名 | 说明 |
|--------|------|
| menu | 下拉菜单内容 |
| default | 下拉框内容 |

---

## 🎯 第三方组件使用建议

### 1. 安装建议
- ✅ 按需安装，只安装需要的组件
- ✅ 使用pnpm或yarn管理依赖
- ✅ 定期检查更新

### 2. 使用建议
- ✅ 仔细阅读组件文档
- ✅ 注意平台兼容性
- ✅ 处理好异步操作
- ✅ 及时处理错误情况

### 3. 性能建议
- ✅ 避免重复引入
- ✅ 合理使用懒加载
- ✅ 注意内存释放

---

## 📦 组件对照表

| 组件名 | npm包名 | 主要用途 | 平台支持 |
|--------|---------|----------|----------|
| TnSuspendButton | tnuiv3p-tn-suspend-button | 悬浮按钮 | 全平台 |
| TnImageCrop | tnuiv3p-tn-image-crop | 图片裁剪 | 全平台 |
| TnSignBoard | tnuiv3p-tn-sign-board | 签名板 | 全平台 |
| TnColorSelect | tnuiv3p-tn-color-select | 颜色选择器 | 全平台 |
| TnStackSwiper | tnuiv3p-tn-stack-swiper | 堆叠轮播 | 全平台 |
| TnVerifyCodeInput | tnuiv3p-tn-verify-code-input | 验证码输入 | 全平台 |
| TnUpdateUserInfoPopup | tnuiv3p-tn-update-user-info-popup | 用户信息弹框 | 全平台 |
| TnDropdown | tnuiv3p-tn-dropdown | 下拉框 | 全平台 |

---

## 🔗 更多第三方组件

根据官方文档，还有以下第三方组件正在开发或即将发布：
- 时间轴组件
- 评论列表组件
- 酷炫图标组件
- 图文卡片组件
- 标签选择组件
- 隐私弹框组件

请访问官方文档了解最新的第三方组件信息：https://vue3.tuniaokj.com/doc/third-component/

---

## 💡 开发自己的第三方组件

如果你想为图鸟UI开发第三方组件：

1. **联系官方**
   - 微信：`tnkewo`
   - 备注：tuniaoUI vue3 插件开发

2. **开发规范**
   - 遵循图鸟UI的设计规范
   - 提供完整的TypeScript类型定义
   - 编写详细的文档和示例
   - 确保多平台兼容性

3. **发布流程**
   - 发布到npm仓库
   - 提交到GitHub
   - 提供完整的README文档
   - 联系官方收录

---

## 📚 相关资源

- 官方文档：https://vue3.tuniaokj.com
- GitHub组织：https://github.com/HighSpecific
- npm搜索：https://www.npmjs.com/search?q=tnuiv3p

---

**更新日志**：请查看各组件的GitHub仓库了解最新更新

**技术支持**：请在对应组件的GitHub仓库提Issue

---

_最后更新：2025-10-27_

