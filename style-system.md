# 图鸟UI Vue3 样式系统完整指南

## 颜色系统

### 内置颜色变量

图鸟UI提供了丰富的内置颜色变量，所有颜色变量以 `tn-` 开头：

#### 主题色系
- `tn-blue` - 蓝色系
  - `tn-blue-light` - 浅蓝色
  - `tn-blue-dark` - 深蓝色
- `tn-red` - 红色系
  - `tn-red-light` - 浅红色
  - `tn-red-dark` - 深红色
- `tn-green` - 绿色系
  - `tn-green-light` - 浅绿色
  - `tn-green-dark` - 深绿色
- `tn-yellow` - 黄色系
  - `tn-yellow-light` - 浅黄色
  - `tn-yellow-dark` - 深黄色
- `tn-orange` - 橙色系
  - `tn-orange-light` - 浅橙色
  - `tn-orange-dark` - 深橙色
- `tn-purple` - 紫色系
  - `tn-purple-light` - 浅紫色
  - `tn-purple-dark` - 深紫色

#### 中性色系
- `tn-grey` - 灰色
  - `tn-grey-light` - 浅灰色
  - `tn-grey-dark` - 深灰色
  - `tn-grey-disabled` - 禁用灰色
- `tn-white` - 白色
- `tn-black` - 黑色

#### 渐变色系
图鸟UI提供了多种渐变色，使用格式为 `gradient__<name>`：

- `gradient__cool-1` - 酷炫渐变1
- `gradient__cool-2` - 酷炫渐变2
- `gradient__cool-3` - 酷炫渐变3
- `gradient__cool-4` - 酷炫渐变4
- `gradient__cool-5` - 酷炫渐变5
- `gradient__cool-6` - 酷炫渐变6
- `gradient__teal` - 青色渐变

### 颜色使用方式

#### 1. 背景色
```vue
<!-- 使用内置颜色 -->
<view class="tn-blue_bg">蓝色背景</view>
<view class="tn-red_bg">红色背景</view>

<!-- 通过组件属性设置 -->
<TnButton bg-color="tn-blue">蓝色按钮</TnButton>
<TnButton bg-color="gradient__cool-1">渐变按钮</TnButton>

<!-- 使用标准颜色值 -->
<TnButton bg-color="#01beff">自定义颜色</TnButton>
<TnButton bg-color="rgb(1, 190, 255)">RGB颜色</TnButton>
<TnButton bg-color="rgba(1, 190, 255, 0.5)">RGBA颜色</TnButton>
```

#### 2. 文字颜色
```vue
<!-- 使用内置颜色类 -->
<view class="tn-blue_text">蓝色文字</view>
<view class="tn-red_text">红色文字</view>
<view class="tn-gray_text">灰色文字</view>

<!-- 通过组件属性设置 -->
<TnButton text-color="tn-blue">蓝色文字</TnButton>
<TnButton text-color="#01beff">自定义文字颜色</TnButton>
```

#### 3. 边框颜色
```vue
<!-- 使用内置边框 -->
<view class="tn-border">默认边框</view>
<view class="tn-border tn-border-bold">加粗边框</view>
<view class="tn-border tn-border-dashed">虚线边框</view>

<!-- 指定方向边框 -->
<view class="tn-border-top">上边框</view>
<view class="tn-border-right">右边框</view>
<view class="tn-border-bottom">下边框</view>
<view class="tn-border-left">左边框</view>
```

---

## 尺寸系统

### 组件尺寸

大多数组件支持统一的尺寸规格：

- `sm` - 小尺寸
- 默认尺寸（不设置size属性）
- `lg` - 大尺寸
- `xl` - 超大尺寸

**使用示例**
```vue
<!-- 按钮尺寸 -->
<TnButton size="sm">小按钮</TnButton>
<TnButton>默认按钮</TnButton>
<TnButton size="lg">大按钮</TnButton>
<TnButton size="xl">超大按钮</TnButton>

<!-- 输入框尺寸 -->
<TnInput size="sm" placeholder="小输入框" />
<TnInput size="lg" placeholder="大输入框" />

<!-- 图标尺寸 -->
<TnIcon name="logo-tuniao" size="20" />
<TnIcon name="logo-tuniao" size="40rpx" />
<TnIcon name="logo-tuniao" size="2em" />
```

### 自定义尺寸

除了预设尺寸，组件还支持传入具体数值：

```vue
<!-- 数字(默认单位rpx) -->
<TnButton width="200" height="80">自定义大小</TnButton>

<!-- 带单位的字符串 -->
<TnButton width="200px" height="80px">像素单位</TnButton>
<TnButton width="50%" height="40rpx">百分比单位</TnButton>
<TnButton width="10vw" height="5vh">视口单位</TnButton>
```

---

## 间距系统

### Padding - 内边距

#### 全方向内边距
```vue
<view class="tn-p">默认内边距</view>
<view class="tn-p-xs">超小内边距</view>
<view class="tn-p-sm">小内边距</view>
<view class="tn-p-lg">大内边距</view>
<view class="tn-p-xl">超大内边距</view>
```

#### 单边内边距
```vue
<!-- 上内边距 -->
<view class="tn-pt">上内边距</view>
<view class="tn-pt-xs">超小上内边距</view>
<view class="tn-pt-sm">小上内边距</view>

<!-- 右内边距 -->
<view class="tn-pr">右内边距</view>
<view class="tn-pr-lg">大右内边距</view>

<!-- 下内边距 -->
<view class="tn-pb">下内边距</view>
<view class="tn-pb-xl">超大下内边距</view>

<!-- 左内边距 -->
<view class="tn-pl">左内边距</view>
<view class="tn-pl-sm">小左内边距</view>
```

### Margin - 外边距

#### 全方向外边距
```vue
<view class="tn-m">默认外边距</view>
<view class="tn-m-xs">超小外边距</view>
<view class="tn-m-sm">小外边距</view>
<view class="tn-m-lg">大外边距</view>
<view class="tn-m-xl">超大外边距</view>
```

#### 单边外边距
```vue
<!-- 上外边距 -->
<view class="tn-mt">上外边距</view>
<view class="tn-mt-xs">超小上外边距</view>

<!-- 右外边距 -->
<view class="tn-mr">右外边距</view>
<view class="tn-mr-lg">大右外边距</view>

<!-- 下外边距 -->
<view class="tn-mb">下外边距</view>
<view class="tn-mb-xl">超大下外边距</view>

<!-- 左外边距 -->
<view class="tn-ml">左外边距</view>
<view class="tn-ml-sm">小左外边距</view>
```

---

## 布局系统

### Flex布局

#### 基础Flex类
```vue
<!-- Flex容器 -->
<view class="tn-flex">Flex容器</view>

<!-- Flex方向 -->
<view class="tn-flex tn-flex-row">横向排列(默认)</view>
<view class="tn-flex tn-flex-column">纵向排列</view>

<!-- 主轴对齐 -->
<view class="tn-flex tn-flex-start">起始对齐</view>
<view class="tn-flex tn-flex-center">居中对齐</view>
<view class="tn-flex tn-flex-end">末尾对齐</view>
<view class="tn-flex tn-flex-between">两端对齐</view>
<view class="tn-flex tn-flex-around">环绕对齐</view>

<!-- 交叉轴对齐 -->
<view class="tn-flex tn-align-start">起始对齐</view>
<view class="tn-flex tn-align-center">居中对齐</view>
<view class="tn-flex tn-align-end">末尾对齐</view>

<!-- 常用组合 -->
<view class="tn-flex-center">完全居中</view>
<view class="tn-flex-column tn-flex-center">纵向完全居中</view>
```

#### Flex项目
```vue
<!-- Flex比例 -->
<view class="tn-flex">
  <view class="tn-flex-1">占1份</view>
  <view class="tn-flex-2">占2份</view>
  <view class="tn-flex-3">占3份</view>
</view>
```

### 宽度系统

```vue
<!-- 百分比宽度 -->
<view class="tn-w-full">100%宽度</view>
<view class="tn-w-50">50%宽度</view>

<!-- 固定宽度类 -->
<view class="tn-w-100">100rpx宽度</view>
<view class="tn-w-200">200rpx宽度</view>
```

### 高度系统

```vue
<!-- 百分比高度 -->
<view class="tn-h-full">100%高度</view>
<view class="tn-h-screen">100vh高度</view>

<!-- 固定高度类 -->
<view class="tn-h-100">100rpx高度</view>
<view class="tn-h-200">200rpx高度</view>
```

---

## 边框系统

### 基础边框
```vue
<!-- 显示边框 -->
<view class="tn-border">默认边框</view>
<view class="tn-border tn-border-bold">加粗边框</view>
<view class="tn-border tn-border-dashed">虚线边框</view>
```

### 单边边框
```vue
<view class="tn-border-top">上边框</view>
<view class="tn-border-right">右边框</view>
<view class="tn-border-bottom">下边框</view>
<view class="tn-border-left">左边框</view>
```

### 边框圆角
```vue
<!-- 圆角类 -->
<view class="tn-radius">默认圆角</view>
<view class="tn-radius-sm">小圆角</view>
<view class="tn-radius-lg">大圆角</view>
<view class="tn-radius-xl">超大圆角</view>
<view class="tn-radius-circle">圆形</view>

<!-- 单角圆角 -->
<view class="tn-radius-top-left">左上圆角</view>
<view class="tn-radius-top-right">右上圆角</view>
<view class="tn-radius-bottom-left">左下圆角</view>
<view class="tn-radius-bottom-right">右下圆角</view>
```

---

## 阴影系统

### 基础阴影
```vue
<!-- 默认阴影 -->
<view class="tn-shadow">默认阴影</view>

<!-- 不同程度的阴影 -->
<view class="tn-shadow-sm">小阴影</view>
<view class="tn-shadow-lg">大阴影</view>
<view class="tn-shadow-xl">超大阴影</view>

<!-- 模糊阴影 -->
<view class="tn-shadow-blur">模糊阴影</view>
```

### 通过组件属性设置阴影
```vue
<!-- 按钮阴影 -->
<TnButton shadow shadow-color="tn-gray">有阴影的按钮</TnButton>

<!-- 自定义阴影颜色 -->
<TnButton shadow shadow-color="#01beff">蓝色阴影</TnButton>
<TnButton shadow shadow-color="rgba(1, 190, 255, 0.3)">半透明阴影</TnButton>
```

---

## 文本样式系统

### 文字大小
```vue
<!-- 使用类名 -->
<view class="tn-text-xs">超小文字</view>
<view class="tn-text-sm">小文字</view>
<view class="tn-text-base">基础文字</view>
<view class="tn-text-lg">大文字</view>
<view class="tn-text-xl">超大文字</view>
<view class="tn-text-2xl">2倍大文字</view>

<!-- 通过组件属性 -->
<TnButton font-size="28">28rpx文字</TnButton>
<TnButton font-size="28px">28px文字</TnButton>
```

### 文字粗细
```vue
<!-- 使用类名 -->
<view class="tn-text-bold">加粗文字</view>
<view class="tn-text-normal">正常文字</view>

<!-- 通过组件属性 -->
<TnButton bold>加粗按钮</TnButton>
<TnIcon name="logo-tuniao" bold />
```

### 文字对齐
```vue
<view class="tn-text-left">左对齐</view>
<view class="tn-text-center">居中对齐</view>
<view class="tn-text-right">右对齐</view>
```

### 文字颜色
```vue
<!-- 使用内置颜色类 -->
<view class="tn-blue_text">蓝色文字</view>
<view class="tn-red_text">红色文字</view>
<view class="tn-gray_text">灰色文字</view>

<!-- 主题色 -->
<view class="tn-color-primary">主题色文字</view>
<view class="tn-color-success">成功色文字</view>
<view class="tn-color-warning">警告色文字</view>
<view class="tn-color-danger">危险色文字</view>
<view class="tn-color-info">信息色文字</view>
```

---

## 常用组合样式

### 1. 卡片样式
```vue
<view class="tn-white_bg tn-radius tn-shadow tn-p">
  卡片内容
</view>

<!-- 带边框的卡片 -->
<view class="tn-white_bg tn-radius tn-border tn-p">
  卡片内容
</view>
```

### 2. 列表项样式
```vue
<view class="tn-white_bg tn-p tn-border-bottom">
  <view class="tn-flex tn-align-center">
    <TnIcon name="user" />
    <view class="tn-ml">用户信息</view>
  </view>
</view>
```

### 3. 居中布局
```vue
<!-- 水平垂直居中 -->
<view class="tn-flex-center">
  完全居中的内容
</view>

<!-- 纵向居中 -->
<view class="tn-flex-column tn-flex-center">
  <view>第一行</view>
  <view>第二行</view>
</view>
```

### 4. 按钮组
```vue
<view class="tn-flex tn-flex-center">
  <TnButton class="tn-mr-sm">按钮1</TnButton>
  <TnButton class="tn-mr-sm">按钮2</TnButton>
  <TnButton>按钮3</TnButton>
</view>
```

### 5. 表单项布局
```vue
<view class="tn-p">
  <view class="tn-mb">
    <TnInput placeholder="用户名" />
  </view>
  <view class="tn-mb">
    <TnInput type="password" placeholder="密码" />
  </view>
  <view class="tn-mt-lg">
    <TnButton type="primary" width="100%">登录</TnButton>
  </view>
</view>
```

---

## 主题定制

### 通过CSS变量定制主题

图鸟UI使用CSS变量来管理主题色，可以通过覆盖这些变量来自定义主题：

```scss
// 在App.vue或全局样式文件中
page {
  // 主题色
  --tn-color-primary: #01beff;
  --tn-color-success: #09bb07;
  --tn-color-warning: #ff976a;
  --tn-color-danger: #f56c6c;
  --tn-color-info: #909399;
  
  // 文字颜色
  --tn-text-color-primary: #303133;
  --tn-text-color-regular: #606266;
  --tn-text-color-secondary: #909399;
  --tn-text-color-placeholder: #c0c4cc;
  
  // 边框颜色
  --tn-border-color: #e4e7ed;
  --tn-border-color-light: #ebeef5;
  --tn-border-color-lighter: #f2f6fc;
  
  // 背景颜色
  --tn-bg-color: #ffffff;
  --tn-bg-color-light: #f5f7fa;
  --tn-bg-color-lighter: #fafafa;
}
```

### 组件级别样式定制

#### 方式一：使用custom-style属性
```vue
<script setup>
import type { CSSProperties } from 'vue'

const customStyle: CSSProperties = {
  fontSize: '32rpx',
  color: '#01beff',
  backgroundColor: 'rgba(1, 190, 255, 0.1)',
  borderRadius: '20rpx',
}
</script>

<template>
  <TnButton :custom-style="customStyle">自定义样式按钮</TnButton>
</template>
```

#### 方式二：使用custom-class属性
```vue
<template>
  <TnButton custom-class="my-button">自定义类名按钮</TnButton>
</template>

<style lang="scss">
.my-button {
  font-size: 32rpx;
  color: #01beff;
  background-color: rgba(1, 190, 255, 0.1);
  border-radius: 20rpx;
}
</style>
```

---

## 响应式设计

### 使用rpx单位
图鸟UI默认使用rpx作为单位，可以自动适配不同屏幕尺寸：

```vue
<!-- rpx会根据屏幕宽度自动缩放 -->
<TnButton width="200" height="80">按钮</TnButton>

<!-- 等同于 -->
<TnButton width="200rpx" height="80rpx">按钮</TnButton>
```

### 百分比布局
```vue
<view class="tn-flex">
  <view class="tn-flex-1">占50%</view>
  <view class="tn-flex-1">占50%</view>
</view>

<TnButton width="100%">全宽按钮</TnButton>
<TnButton width="80%">80%宽度按钮</TnButton>
```

---

## 动画与过渡

### 内置过渡效果

组件内置了平滑的过渡动画：

```vue
<!-- 弹出框过渡 -->
<TnPopup v-model="show" :duration="300">
  内容
</TnPopup>

<!-- 遮罩层过渡 -->
<TnOverlay v-model:show="show" :duration="250" />

<!-- 加载图标动画 -->
<TnLoading show animation duration="2" time-function="ease-in-out" />
```

### 自定义动画时长
```vue
<!-- 数字跳转动画 -->
<TnCountTo start="0" end="100" :duration="2000" />

<!-- 数字滚动动画 -->
<TnCountScroll value="7865.23" :duration="1500" />

<!-- 倒计时 -->
<TnCountDown :time="300" />
```

---

## 平台特定样式

### 安全区域适配

```vue
<!-- 底部安全区域 -->
<TnPopup 
  v-model="show" 
  open-direction="bottom"
  safe-area-inset-bottom
>
  内容
</TnPopup>

<!-- 导航栏安全区域 -->
<TnTabbar fixed safe-area-inset-bottom>
  <TnTabbarItem text="首页" />
</TnTabbar>
```

### 微信小程序特殊处理

对于微信小程序平台，组件提供了 `custom-class` 和 `custom-style` 属性：

```vue
<template>
  <!-- 微信小程序需要使用custom-class -->
  <TnButton custom-class="my-btn" :custom-style="btnStyle">
    按钮
  </TnButton>
</template>

<script setup>
const btnStyle = {
  fontSize: '28rpx',
  backgroundColor: '#01beff',
}
</script>
```

---

## 最佳实践

### 1. 颜色使用建议
- ✅ 优先使用内置主题色：`primary`、`success`、`warning`、`danger`、`info`
- ✅ 使用内置颜色变量：`tn-blue`、`tn-red`等
- ✅ 使用渐变色增强视觉效果：`gradient__cool-1`
- ⚠️ 避免硬编码hex颜色，不利于主题切换

### 2. 尺寸使用建议
- ✅ 优先使用预设尺寸：`sm`、`lg`、`xl`
- ✅ 使用rpx单位保证多端一致
- ✅ 重要文字使用px确保可读性
- ⚠️ 避免使用过小的尺寸影响用户体验

### 3. 间距使用建议
- ✅ 使用内置间距类：`tn-p`、`tn-m`系列
- ✅ 保持间距的一致性
- ✅ 使用合适的间距层级
- ⚠️ 避免过大或过小的间距

### 4. 布局使用建议
- ✅ 优先使用Flex布局
- ✅ 使用`tn-flex-center`快速居中
- ✅ 使用`tn-flex-1`实现自适应
- ⚠️ 注意Flex在不同平台的兼容性

### 5. 组件组合建议
```vue
<!-- 好的示例：语义清晰 -->
<view class="tn-white_bg tn-radius tn-shadow tn-p">
  <view class="tn-flex tn-align-center tn-mb">
    <TnIcon name="user" class="tn-mr-sm" />
    <view class="tn-flex-1">用户名</view>
  </view>
  <TnButton type="primary" width="100%">确定</TnButton>
</view>

<!-- 不好的示例：样式堆叠过多 -->
<view style="background: #fff; padding: 20rpx; margin: 10rpx; border-radius: 15rpx; box-shadow: 0 0 10rpx rgba(0,0,0,0.1);">
  内容
</view>
```

---

## 常用UI模式

### 1. 表单页面模式
```vue
<template>
  <view class="form-container">
    <TnForm ref="formRef" :model="formData" :rules="formRules">
      <TnFormItem label="用户名" prop="username">
        <TnInput v-model="formData.username" placeholder="请输入用户名" />
      </TnFormItem>
      
      <TnFormItem label="密码" prop="password">
        <TnInput v-model="formData.password" type="password" placeholder="请输入密码" />
      </TnFormItem>
      
      <TnFormItem label="性别" prop="gender">
        <TnRadioGroup v-model="formData.gender">
          <TnRadio label="male">男</TnRadio>
          <TnRadio label="female">女</TnRadio>
        </TnRadioGroup>
      </TnFormItem>
    </TnForm>
    
    <view class="tn-p tn-mt-lg">
      <TnButton type="primary" width="100%" @click="submitForm">提交</TnButton>
    </view>
  </view>
</template>

<style lang="scss" scoped>
.form-container {
  padding: 30rpx;
  background: #f5f7fa;
  min-height: 100vh;
}
</style>
```

### 2. 列表页面模式
```vue
<template>
  <view class="list-container">
    <TnListItem
      v-for="item in listData"
      :key="item.id"
      bottom-border
      bottom-border-indent
      @click="handleItemClick(item)"
    >
      <view class="tn-flex tn-align-center">
        <TnAvatar :url="item.avatar" class="tn-mr" />
        <view class="tn-flex-1">
          <view class="tn-text-lg tn-mb-xs">{{ item.name }}</view>
          <view class="tn-gray_text tn-text-sm">{{ item.desc }}</view>
        </view>
        <TnIcon name="right" color="tn-gray" />
      </view>
    </TnListItem>
  </view>
</template>
```

### 3. 卡片列表模式
```vue
<template>
  <view class="card-list">
    <view
      v-for="item in cardData"
      :key="item.id"
      class="card-item tn-white_bg tn-radius tn-shadow tn-p tn-mb"
    >
      <view class="tn-flex tn-align-center tn-mb">
        <view class="tn-flex-1 tn-text-lg tn-text-bold">{{ item.title }}</view>
        <TnTag :type="item.tagType">{{ item.tag }}</TnTag>
      </view>
      <view class="tn-gray_text tn-text-sm">{{ item.content }}</view>
    </view>
  </view>
</template>

<style lang="scss" scoped>
.card-list {
  padding: 30rpx;
  
  .card-item {
    &:last-child {
      margin-bottom: 0;
    }
  }
}
</style>
```

### 4. 底部操作栏模式
```vue
<template>
  <view class="page-container">
    <!-- 页面内容 -->
    <view class="content">
      内容区域
    </view>
    
    <!-- 底部操作栏 -->
    <view class="bottom-bar tn-white_bg tn-p tn-border-top">
      <view class="tn-flex tn-align-center">
        <view class="tn-flex-1 tn-mr">
          <view class="tn-text-lg tn-text-bold tn-red_text">¥99.00</view>
        </view>
        <TnButton type="primary" width="200rpx">立即购买</TnButton>
      </view>
    </view>
  </view>
</template>

<style lang="scss" scoped>
.page-container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  
  .content {
    flex: 1;
    overflow-y: auto;
  }
  
  .bottom-bar {
    flex-shrink: 0;
  }
}
</style>
```

### 5. 网格布局模式
```vue
<template>
  <view class="grid-container">
    <view
      v-for="item in gridData"
      :key="item.id"
      class="grid-item tn-white_bg tn-radius tn-shadow tn-p tn-flex-center tn-flex-column"
    >
      <TnIcon :name="item.icon" size="60" :color="item.color" />
      <view class="tn-mt-sm">{{ item.name }}</view>
    </view>
  </view>
</template>

<style lang="scss" scoped>
.grid-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20rpx;
  padding: 30rpx;
  
  .grid-item {
    aspect-ratio: 1;
  }
}
</style>
```

---

## 暗黑模式支持

### 启用暗黑模式

```scss
// 定义暗黑模式变量
@media (prefers-color-scheme: dark) {
  page {
    --tn-bg-color: #1a1a1a;
    --tn-text-color-primary: #ffffff;
    --tn-text-color-regular: #e0e0e0;
    --tn-border-color: #333333;
  }
}
```

### 组件暗黑模式适配
```vue
<template>
  <!-- 使用CSS变量，自动适配暗黑模式 -->
  <view class="tn-white_bg tn-p">
    内容会根据主题自动调整
  </view>
  
  <!-- 手动指定暗黑模式样式 -->
  <TnButton 
    :bg-color="isDark ? '#333' : '#fff'"
    :text-color="isDark ? '#fff' : '#333'"
  >
    按钮
  </TnButton>
</template>
```

---

## 性能优化建议

### 1. 样式复用
```vue
<!-- 不推荐：重复定义样式 -->
<view style="padding: 30rpx; background: #fff; border-radius: 15rpx;">内容1</view>
<view style="padding: 30rpx; background: #fff; border-radius: 15rpx;">内容2</view>

<!-- 推荐：使用类名复用 -->
<view class="card">内容1</view>
<view class="card">内容2</view>

<style lang="scss" scoped>
.card {
  padding: 30rpx;
  background: #fff;
  border-radius: 15rpx;
}
</style>
```

### 2. 避免深层嵌套
```vue
<!-- 不推荐：过深的嵌套 -->
<view class="tn-flex">
  <view class="tn-flex-1">
    <view class="tn-p">
      <view class="tn-white_bg">
        <view class="tn-radius">
          内容
        </view>
      </view>
    </view>
  </view>
</view>

<!-- 推荐：扁平化结构 -->
<view class="content-box tn-white_bg tn-radius tn-p">
  内容
</view>
```

### 3. 使用v-show替代v-if
```vue
<!-- 频繁切换的内容使用v-show -->
<TnPopup v-show="show">
  内容
</TnPopup>

<!-- 条件渲染使用v-if -->
<TnButton v-if="hasPermission">
  按钮
</TnButton>
```

---

## 常见问题与解决方案

### 1. 组件样式不生效

**问题**: 在微信小程序中设置组件样式不生效

**解决方案**: 使用`custom-class`和`custom-style`属性
```vue
<TnButton custom-class="my-btn" :custom-style="{ fontSize: '32rpx' }">
  按钮
</TnButton>
```

### 2. 边框显示异常

**问题**: 边框在某些情况下显示不完整

**解决方案**: 确保使用正确的边框类
```vue
<!-- 正确 -->
<view class="tn-border">内容</view>

<!-- 单边边框 -->
<view class="tn-border-bottom">内容</view>
```

### 3. 颜色渐变不生效

**问题**: 某些组件不支持渐变色

**解决方案**: 检查组件文档，部分组件（如Switch、Slider）只支持普通颜色
```vue
<!-- Switch不支持渐变色 -->
<TnSwitch active-color="tn-blue" />

<!-- Button支持渐变色 -->
<TnButton bg-color="gradient__cool-1">按钮</TnButton>
```

### 4. 间距设置无效

**问题**: 设置margin或padding不生效

**解决方案**: 使用内置间距类或确保单位正确
```vue
<!-- 推荐 -->
<view class="tn-p tn-mt">内容</view>

<!-- 或使用组件custom-style -->
<TnButton :custom-style="{ margin: '20rpx' }">按钮</TnButton>
```

---

## 样式速查表

### 背景色类名
- `tn-white_bg` - 白色背景
- `tn-blue_bg` - 蓝色背景
- `tn-red_bg` - 红色背景
- `tn-green_bg` - 绿色背景
- `tn-yellow_bg` - 黄色背景
- `tn-grey_bg` - 灰色背景
- `tn-grey-light_bg` - 浅灰色背景

### 文字颜色类名
- `tn-white_text` - 白色文字
- `tn-blue_text` - 蓝色文字
- `tn-red_text` - 红色文字
- `tn-green_text` - 绿色文字
- `tn-gray_text` - 灰色文字
- `tn-grey-disabled_text` - 禁用灰色文字

### Flex布局类名
- `tn-flex` - Flex容器
- `tn-flex-center` - 完全居中
- `tn-flex-column` - 纵向布局
- `tn-flex-1` - flex: 1
- `tn-flex-between` - 两端对齐
- `tn-align-center` - 交叉轴居中

### 间距类名
- `tn-p` - 默认内边距
- `tn-p-xs/sm/lg/xl` - 不同大小内边距
- `tn-m` - 默认外边距  
- `tn-m-xs/sm/lg/xl` - 不同大小外边距
- `tn-pt/pr/pb/pl` - 单边内边距
- `tn-mt/mr/mb/ml` - 单边外边距

### 边框类名
- `tn-border` - 默认边框
- `tn-border-bold` - 加粗边框
- `tn-border-dashed` - 虚线边框
- `tn-border-top/right/bottom/left` - 单边边框
- `tn-radius` - 默认圆角
- `tn-radius-circle` - 圆形

### 阴影类名
- `tn-shadow` - 默认阴影
- `tn-shadow-sm/lg/xl` - 不同大小阴影
- `tn-shadow-blur` - 模糊阴影

---

## 总结

图鸟UI Vue3提供了完善的样式系统，包括：

1. **颜色系统** - 内置丰富的颜色变量和渐变色
2. **尺寸系统** - 统一的组件尺寸规范
3. **间距系统** - 完整的padding和margin工具类
4. **布局系统** - 强大的Flex布局支持
5. **边框系统** - 灵活的边框和圆角设置
6. **阴影系统** - 多层级阴影效果
7. **主题定制** - 支持CSS变量自定义主题
8. **响应式设计** - rpx单位自动适配

通过合理使用这些样式系统，可以快速构建美观、一致的用户界面。

