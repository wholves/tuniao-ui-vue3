# 图鸟UI Vue3 资源与模板

> 📦 图鸟UI提供的资源、模板和工具  
> 📅 更新时间：2025-10-27  
> 🔗 官方网站：https://vue3.tuniaokj.com

## 📚 资源概览

图鸟UI为开发者提供了丰富的资源，包括：
- 🎨 UI设计资源
- 📱 页面模板
- 🛠️ 开发工具
- 📖 示例项目
- 🎓 学习资源

---

## 🎨 UI设计资源

### Logo资源
- 图鸟Logo SVG：https://vue3.tuniaokj.com/images/tuniao-logo.svg
- 适用于：应用图标、文档、宣传材料

### 特性图片
根据官网首页展示，图鸟UI提供以下特性图片：
- https://vue3.tuniaokj.com/images/home/features/A1.jpg - 指南特性图
- https://vue3.tuniaokj.com/images/home/features/A2.jpg - 组件特性图
- https://vue3.tuniaokj.com/images/home/features/A3.jpg - 模板特性图
- https://vue3.tuniaokj.com/images/home/features/A4.jpg - 资源特性图

### 示例图片资源
图鸟UI在示例中使用的图片资源：
- 头像图片：https://tnuiimage.tnkjapp.com/avatar/normal/[1-9].png
- Logo图片：https://tnuiimage.tnkjapp.com/logo/tuniao.png
- 轮播图片：
  - https://resource.tuniaokj.com/images/xiongjie/x14.jpg
  - https://resource.tuniaokj.com/images/xiongjie/xiong-3d-2.jpg
  - https://resource.tuniaokj.com/images/xiongjie/xiong-3d-new.jpg
  - https://resource.tuniaokj.com/images/xiongjie/xiong-3d-new1.png
  - https://resource.tuniaokj.com/images/xiongjie/xiong-3d.jpg
- 内容图片：https://resource.tuniaokj.com/images/content/rodion.jpg

---

## 📱 页面模板

### 官方模板项目

#### CLI模板项目
图鸟UI提供了完整的CLI模板项目，包含了常用的页面和功能示例。

**GitHub地址**：
```
https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template
```

**Gitee地址**：
```
https://gitee.com/TSpecific/tuniao-ui-vue3-uniapp-template
```

**下载方式**：
```bash
# 从GitHub克隆
git clone https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template

# 从Gitee克隆
git clone https://gitee.com/TSpecific/tuniao-ui-vue3-uniapp-template
```

#### 演示项目源码
**GitHub地址**：
```
https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo
```

**包含内容**：
- ✅ 所有组件的演示页面
- ✅ 常用页面模板
- ✅ 完整的项目结构
- ✅ 最佳实践示例

### 模板特点

根据官网描述，图鸟UI的模板具有以下特点：
- 🎨 **酷炫设计** - 让你眼前一亮的界面效果
- 📱 **多端适配** - 适配微信小程序、APP、H5
- 🚀 **开箱即用** - 快速集成，即刻使用
- 💡 **最佳实践** - 遵循最佳开发实践

### 常见页面模板

根据组件库功能，可以实现以下常见页面模板：

#### 1. 登录注册页面
**涉及组件**：
- TnForm + TnFormItem
- TnInput
- TnButton
- TnCheckbox
- TnModal

#### 2. 个人中心页面
**涉及组件**：
- TnAvatar
- TnListItem
- TnBadge
- TnIcon
- TnNavbar

#### 3. 商品列表页面
**涉及组件**：
- TnWaterFall
- TnPhotoAlbum
- TnTag
- TnLoadmore
- TnSearchBox

#### 4. 商品详情页面
**涉及组件**：
- TnSwiper
- TnTabs
- TnReadMore
- TnButton
- TnNumberBox

#### 5. 购物车页面
**涉及组件**：
- TnSwipeAction
- TnCheckbox
- TnNumberBox
- TnButton

#### 6. 订单页面
**涉及组件**：
- TnSteps
- TnTag
- TnCountDown
- TnListItem

#### 7. 搜索页面
**涉及组件**：
- TnSearchBox
- TnTabs
- TnEmpty
- TnIndexList

#### 8. 表单页面
**涉及组件**：
- TnForm + TnFormItem
- TnInput
- TnPicker
- TnRadio / TnCheckbox
- TnSwitch
- TnSlider
- TnRate

---

## 🛠️ 开发工具

### tuniao-cli 命令行工具

**安装**：
```bash
npm install tuniao-cli -g
```

**功能**：
- ✅ 快速创建项目
- ✅ 自动配置开发环境
- ✅ 集成最新版本的TuniaoUI
- ✅ 提供项目模板

**使用**：
```bash
# 创建项目
tuniao create my-project

# 查看帮助
tuniao --help

# 查看版本
tuniao --version
```

**npm地址**：https://www.npmjs.com/package/tuniao-cli

---

## 📦 npm包资源

### 核心包

#### @tuniao/tnui-vue3-uniapp
- **用途**：TuniaoUI核心组件库
- **地址**：https://www.npmjs.com/package/@tuniao/tnui-vue3-uniapp
- **安装**：`npm install @tuniao/tnui-vue3-uniapp`

#### @tuniao/tn-icon
- **用途**：图鸟图标字体库
- **地址**：https://www.npmjs.com/package/@tuniao/tn-icon
- **安装**：`npm install @tuniao/tn-icon`
- **特点**：
  - 基于字体图标
  - 重绘常见图标
  - 统一化设计
  - 支持单独使用

#### @tuniao/tn-style
- **用途**：图鸟样式系统
- **地址**：https://www.npmjs.com/package/@tuniao/tn-style
- **安装**：`npm install @tuniao/tn-style`
- **包含**：
  - 颜色系统
  - 间距系统
  - 布局系统
  - 工具类

### 第三方扩展包

所有第三方组件都发布在npm上，包名格式：`tnuiv3p-tn-<component-name>`

| 包名 | 组件名 | 用途 |
|------|--------|------|
| tnuiv3p-tn-suspend-button | TnSuspendButton | 悬浮按钮 |
| tnuiv3p-tn-image-crop | TnImageCrop | 图片裁剪 |
| tnuiv3p-tn-sign-board | TnSignBoard | 签名板 |
| tnuiv3p-tn-color-select | TnColorSelect | 颜色选择器 |
| tnuiv3p-tn-stack-swiper | TnStackSwiper | 堆叠轮播 |
| tnuiv3p-tn-verify-code-input | TnVerifyCodeInput | 验证码输入 |
| tnuiv3p-tn-dropdown | TnDropdown | 下拉框 |
| tnuiv3p-tn-update-user-info-popup | TnUpdateUserInfoPopup | 用户信息弹框 |

---

## 📖 文档资源

### 官方文档
- **Vue3文档**：https://vue3.tuniaokj.com
- **Vue2文档**：https://vue2.tuniaokj.com

### GitHub仓库
- **主仓库**：https://github.com/tuniaoTech/tuniaoui-rc-vue3-uniapp
- **模板仓库**：https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template
- **示例仓库**：https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo

### uni-app插件市场
- **TuniaoUI Vue3**：https://ext.dcloud.net.cn/plugin?id=13530
- **TuniaoUI Vue3 (uni_modules)**：https://ext.dcloud.net.cn/plugin?name=tuniaoui-vue3

---

## 🎓 学习资源

### 官方演示

#### 微信小程序演示
扫描二维码体验（查看官方文档获取二维码）

#### 支付宝小程序演示
扫描二维码体验（查看官方文档获取二维码）

### 视频教程
建议查看官方文档或B站搜索"图鸟UI"获取视频教程

### 社区资源
- QQ群：查看官方文档
- 微信群：查看官方文档
- 官方博客：查看官方网站

---

## 🎨 颜色资源

### 完整颜色列表

根据从官网爬取的样式系统，图鸟UI提供以下颜色：

#### 主题色
- `tn-type-primary` - 主题色
- `tn-type-success` - 成功色
- `tn-type-warning` - 警告色
- `tn-type-danger` - 危险色
- `tn-type-error` - 错误色
- `tn-type-info` - 信息色

#### 内置颜色（每种颜色包含4个变体）
基础色系：
- red (红色)
- purplered (紫红色)
- purple (紫色)
- bluepurple (蓝紫色)
- aquablue (水蓝色)
- blue (蓝色)
- indigo (靛青色)
- cyan (青色)
- teal (青绿色)

绿色系：
- green (绿色)
- yellowgreen (黄绿色)
- lime (青柠色)

黄色系：
- yellow (黄色)
- orangeyellow (橙黄色)

橙色系：
- orange (橙色)
- orangered (橙红色)

其他：
- brown (棕色)
- grey/gray (灰色)

**每种颜色的变体**：
- 标准色：`tn-blue_bg`
- 深色：`tn-blue-dark_bg`
- 浅色：`tn-blue-light_bg`
- 禁用色：`tn-blue-disabled_bg`

#### 渐变色

**普通渐变色**（每种颜色3个变体）：
- 标准渐变：`tn-gradient-bg__blue`
- 浅色渐变：`tn-gradient-bg__blue-light`
- 单色渐变：`tn-gradient-bg__blue-single`

**注意**：orangered、brown、gray只有single变体

**酷炫渐变色**（16种）：
- `tn-gradient-bg__cool-1` 到 `tn-gradient-bg__cool-16`

**带背景图片的渐变色**：
在渐变色类名基础上添加 `tn-bg-image` 类：
```html
<div class="tn-gradient-bg__cool-1 tn-bg-image">带背景图的渐变</div>
```

### 文本颜色

所有背景色都有对应的文本颜色，使用格式：
```html
<!-- 主题色文本 -->
<div class="tn-type-primary_text">主题色文本</div>

<!-- 内置颜色文本 -->
<div class="tn-red_text">红色文本</div>
<div class="tn-blue-light_text">浅蓝色文本</div>
```

---

## 📝 样式工具类

### 文本样式

#### 字体大小
- `tn-text-xs` - 12px
- `tn-text-sm` - 13px
- `tn-text` - 14px (默认)
- `tn-text-lg` - 16px
- `tn-text-xl` - 18px
- `tn-text-2xl` - 20px
- `tn-text-3xl` - 26px
- `tn-text-4xl` - 32px

#### 文本对齐
- `tn-text-left` - 左对齐
- `tn-text-center` - 居中对齐
- `tn-text-right` - 右对齐

#### 文本样式
- `tn-text-bold` - 加粗
- `tn-text-uppercase` - 转大写
- `tn-text-lowercase` - 转小写
- `tn-text-capitalize` - 首字母大写
- `tn-text-transparent` - 透明文字（根据背景自适应）

#### 文本溢出
- `tn-text-ellipsis-1` - 1行溢出隐藏
- `tn-text-ellipsis-2` - 2行溢出隐藏
- `tn-text-ellipsis-3` - 3行溢出隐藏
- `tn-text-ellipsis-4` - 4行溢出隐藏
- `tn-text-ellipsis-5` - 5行溢出隐藏

**注意**：使用溢出隐藏时，容器必须设置宽度！

---

## 🎯 快速开发模板

### 模板1：登录页面
```vue
<script setup lang="ts">
import { reactive, ref } from 'vue'

const formRef = ref()
const formData = reactive({
  username: '',
  password: '',
  remember: false
})

const rules = {
  username: [
    { required: true, message: '请输入用户名', trigger: 'blur' }
  ],
  password: [
    { required: true, message: '请输入密码', trigger: 'blur' },
    { min: 6, message: '密码至少6位', trigger: 'blur' }
  ]
}

const handleLogin = () => {
  formRef.value?.validate((valid) => {
    if (valid) {
      // 登录逻辑
      console.log('登录信息:', formData)
    }
  })
}
</script>

<template>
  <view class="login-page">
    <view class="logo tn-flex-center tn-mb-xl">
      <TnIcon name="logo-tuniao" size="120" color="tn-blue" />
    </view>
    
    <view class="form-container tn-white_bg tn-radius tn-p">
      <TnForm ref="formRef" :model="formData" :rules="rules">
        <TnFormItem label="用户名" prop="username">
          <TnInput v-model="formData.username" placeholder="请输入用户名" clearable />
        </TnFormItem>
        
        <TnFormItem label="密码" prop="password">
          <TnInput v-model="formData.password" type="password" placeholder="请输入密码" />
        </TnFormItem>
        
        <TnFormItem>
          <TnCheckbox v-model="formData.remember">记住密码</TnCheckbox>
        </TnFormItem>
      </TnForm>
      
      <view class="tn-mt-lg">
        <TnButton type="primary" width="100%" @click="handleLogin">登录</TnButton>
      </view>
    </view>
  </view>
</template>

<style lang="scss" scoped>
.login-page {
  min-height: 100vh;
  padding: 60rpx 30rpx;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  
  .form-container {
    box-shadow: 0 10rpx 30rpx rgba(0, 0, 0, 0.1);
  }
}
</style>
```

### 模板2：商品列表页面
```vue
<script setup lang="ts">
import { ref } from 'vue'

const searchKeyword = ref('')
const currentTab = ref(0)
const loadmoreStatus = ref('loadmore')

const productList = ref([
  // 商品数据
])

const handleSearch = (keyword) => {
  console.log('搜索:', keyword)
}

const loadMore = () => {
  // 加载更多逻辑
}
</script>

<template>
  <view class="product-page">
    <!-- 搜索栏 -->
    <view class="search-bar tn-white_bg tn-p">
      <TnSearchBox v-model="searchKeyword" @search="handleSearch" />
    </view>
    
    <!-- 分类标签 -->
    <view class="category-tabs tn-white_bg">
      <TnTabs v-model="currentTab">
        <TnTabsItem title="全部" />
        <TnTabsItem title="热销" />
        <TnTabsItem title="新品" />
      </TnTabs>
    </view>
    
    <!-- 商品列表 -->
    <view class="product-list">
      <TnWaterFall :data="productList" mode="calc">
        <template #left="{ item }">
          <view class="product-card tn-white_bg tn-radius tn-shadow tn-mb">
            <image :src="item.image" mode="widthFix" />
            <view class="tn-p">
              <view class="tn-text-lg tn-text-bold">{{ item.name }}</view>
              <view class="tn-mt-sm">
                <text class="tn-red_text tn-text-xl tn-text-bold">¥{{ item.price }}</text>
              </view>
            </view>
          </view>
        </template>
        
        <template #right="{ item }">
          <!-- 同left -->
        </template>
      </TnWaterFall>
      
      <TnLoadmore :status="loadmoreStatus" @click="loadMore" />
    </view>
  </view>
</template>
```

### 模板3：个人中心页面
```vue
<script setup lang="ts">
import { ref } from 'vue'

const userInfo = ref({
  avatar: 'https://tnuiimage.tnkjapp.com/avatar/normal/1.png',
  nickname: '图鸟用户',
  level: 'VIP',
  points: 9999
})

const menuList = [
  { icon: 'order', name: '我的订单', badge: '5' },
  { icon: 'shop', name: '我的收藏' },
  { icon: 'coupon', name: '优惠券', badge: '3' },
  { icon: 'setting', name: '设置' },
]
</script>

<template>
  <view class="user-page">
    <!-- 用户信息卡片 -->
    <view class="user-card tn-gradient-bg__cool-6 tn-p">
      <view class="tn-flex tn-align-center">
        <TnAvatar :url="userInfo.avatar" size="xl" border border-color="#fff" />
        <view class="tn-ml tn-flex-1 tn-white_text">
          <view class="tn-text-xl tn-text-bold">{{ userInfo.nickname }}</view>
          <view class="tn-mt-xs">
            <TnTag size="sm" bg-color="rgba(255,255,255,0.3)" text-color="#fff">
              {{ userInfo.level }}
            </TnTag>
          </view>
        </view>
        <view class="tn-white_text tn-text-center">
          <view class="tn-text-2xl tn-text-bold">{{ userInfo.points }}</view>
          <view class="tn-text-sm tn-mt-xs">积分</view>
        </view>
      </view>
    </view>
    
    <!-- 功能菜单 -->
    <view class="menu-list tn-white_bg tn-mt">
      <TnListItem
        v-for="(item, index) in menuList"
        :key="index"
        :bottom-border="index < menuList.length - 1"
        bottom-border-indent
        right-icon="right"
      >
        <view class="tn-flex tn-align-center">
          <TnIcon :name="item.icon" size="40" color="tn-blue" class="tn-mr" />
          <view class="tn-flex-1">{{ item.name }}</view>
          <TnBadge v-if="item.badge" :value="item.badge" type="danger" />
        </view>
      </TnListItem>
    </view>
  </view>
</template>
```

---

## 🌈 设计资源

### 颜色方案

#### 推荐配色方案

**方案1：清新蓝**
- 主色：`#01beff` (tn-blue)
- 辅色：`#09bb07` (tn-green)
- 文字：`#303133`
- 背景：`#f5f7fa`

**方案2：活力橙**
- 主色：`#ff976a` (tn-orange)
- 辅色：`#ff0036` (tn-red)
- 文字：`#303133`
- 背景：`#f5f7fa`

**方案3：优雅紫**
- 主色：`#8866ff` (tn-purple)
- 辅色：`#01beff` (tn-blue)
- 文字：`#303133`
- 背景：`#f5f7fa`

**方案4：渐变炫彩**
- 主色：`gradient__cool-1`
- 辅色：`gradient__cool-5`
- 文字：`#ffffff`
- 背景：`#1a1a1a`

### 设计原则

1. **一致性** - 使用统一的颜色、字体、间距
2. **简洁性** - 避免过多的装饰和效果
3. **可读性** - 确保文字清晰易读
4. **响应式** - 适配不同屏幕尺寸

---

## 🔧 开发资源

### 配置文件模板

#### vite.config.ts
```typescript
import { defineConfig } from 'vite'
import uni from '@dcloudio/vite-plugin-uni'

export default defineConfig({
  plugins: [uni()],
  css: {
    preprocessorOptions: {
      scss: {
        additionalData: `@import "@tuniao/tn-style/index.scss";`
      }
    }
  },
  resolve: {
    alias: {
      '@': '/src'
    }
  }
})
```

#### tsconfig.json
```json
{
  "extends": "@vue/tsconfig/tsconfig.json",
  "compilerOptions": {
    "sourceMap": true,
    "baseUrl": ".",
    "paths": {
      "@/*": ["./src/*"]
    },
    "types": [
      "@dcloudio/types",
      "@tuniao/tnui-vue3-uniapp"
    ]
  },
  "include": ["src/**/*.ts", "src/**/*.d.ts", "src/**/*.tsx", "src/**/*.vue"]
}
```

#### pages.json (easycom配置)
```json
{
  "easycom": {
    "autoscan": true,
    "custom": {
      "^Tn(.*)": "@tuniao/tnui-vue3-uniapp/components/$1/src/$1.vue"
    }
  }
}
```

---

## 📦 资源下载清单

### 必备资源
- ✅ 图鸟UI核心包：`@tuniao/tnui-vue3-uniapp`
- ✅ 图鸟图标：`@tuniao/tn-icon`
- ✅ 图鸟样式：`@tuniao/tn-style`
- ✅ CLI工具：`tuniao-cli`

### 可选资源
- ⭐ 第三方组件包（按需安装）
- ⭐ 示例项目源码
- ⭐ 设计素材（查看官方文档）

### 在线资源
- 📖 官方文档：https://vue3.tuniaokj.com
- 💻 GitHub：https://github.com/tuniaoTech
- 📦 npm：https://www.npmjs.com/~tuniao
- 🎬 演示小程序：扫码体验

---

## 🎁 社区贡献资源

### 开发者贡献

感谢以下开发者的贡献：
- [北笙༊](https://github.com/abdukuddus)
- [孟夏乾月](https://github.com/cathcy8869)
- [FelixL-Dev](https://github.com/FelixL-Dev)

### 第三方组件开发者

第三方组件主要由 [HighSpecific](https://github.com/HighSpecific) 团队开发维护。

---

## 🔗 友情链接

根据官网展示的友情链接：
- **ScriptEcho** - 技术社区
- **海狐外卖跑腿系统** - 商业系统

---

## 📞 获取更多资源

### 官方渠道
- **官网**：https://vue3.tuniaokj.com
- **微信**：tnkewo
- **QQ群**：查看官方文档
- **GitHub**：https://github.com/tuniaoTech

### 商业合作
图鸟承接以下业务：
- 小程序开发
- Web开发
- UI设计
- 定制开发

联系方式请查看官方文档。

---

## 📊 资源统计

### 组件资源
- 核心组件：56个
- 第三方组件：8+个
- 示例页面：100+个

### 样式资源
- 颜色变量：100+个
- 渐变色：50+个
- 工具类：200+个

### 文档资源
- 组件文档：56篇
- 指南文档：10+篇
- 示例代码：500+段

---

## 🎨 使用建议

### 1. 颜色使用
- ✅ 优先使用主题色保持一致性
- ✅ 使用渐变色增强视觉效果
- ✅ 注意颜色对比度保证可读性
- ⚠️ 避免使用过多颜色造成视觉混乱

### 2. 组件使用
- ✅ 参考官方示例学习用法
- ✅ 查阅详细文档了解API
- ✅ 使用TypeScript获得类型提示
- ⚠️ 注意不同平台的兼容性

### 3. 模板使用
- ✅ 基于官方模板快速开发
- ✅ 根据业务需求调整样式
- ✅ 保持代码结构清晰
- ⚠️ 不要过度定制偏离原设计

---

## 📝 更新说明

### 获取最新资源
- 定期查看官方文档
- 关注GitHub仓库更新
- 订阅npm包更新通知
- 加入官方社区获取第一手资讯

### 版本更新
查看更新日志：https://vue3.tuniaokj.com/doc/guide/changelog.html

---

## 🌟 资源推荐指数

| 资源类型 | 推荐指数 | 适用场景 |
|----------|----------|----------|
| 官方文档 | ⭐⭐⭐⭐⭐ | 学习和查阅 |
| 示例项目 | ⭐⭐⭐⭐⭐ | 快速上手 |
| CLI工具 | ⭐⭐⭐⭐⭐ | 创建项目 |
| 核心组件包 | ⭐⭐⭐⭐⭐ | 开发必备 |
| 第三方组件 | ⭐⭐⭐⭐ | 功能扩展 |
| 图标库 | ⭐⭐⭐⭐ | UI美化 |
| 样式系统 | ⭐⭐⭐⭐ | 快速开发 |

---

## 💡 总结

图鸟UI为开发者提供了完整的开发资源生态：
- 📦 **完整的组件库** - 56+核心组件
- 🎨 **丰富的样式系统** - 100+颜色变量，200+工具类
- 🛠️ **便捷的开发工具** - CLI工具，项目模板
- 📖 **详尽的文档** - 组件文档，指南文档
- 🔌 **可扩展的生态** - 第三方组件支持
- 🎓 **学习资源** - 示例项目，演示程序

立即开始使用图鸟UI，快速构建美观的跨平台应用！🚀

---

_最后更新：2025-10-27_  
_数据来源：https://vue3.tuniaokj.com_

