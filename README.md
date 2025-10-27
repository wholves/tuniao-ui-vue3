# 图鸟UI Vue3 知识库

> 🎉 图鸟UI Vue3 完整组件库知识库  
> 📅 数据采集时间：2025-10-27  
> 🔗 官方网站：https://vue3.tuniaokj.com  
> 📦 组件总数：56个

## 📚 知识库内容

本知识库包含了图鸟UI Vue3版本的完整组件文档、样式系统和使用指南。

### 📂 文件说明

| 文件名 | 说明 | 适用场景 |
|--------|------|----------|
| `tuniao-ui-knowledge-base.md` | **核心知识库** | 快速了解所有组件概览 |
| `components-detail.md` | **详细组件文档** | 查看完整的Props、Events、Slots等API |
| `style-system.md` | **样式系统指南** | 学习颜色、间距、布局等样式系统 |
| `quick-reference.md` | **快速参考手册** | 常用代码片段和快速查询 |
| `components-index.json` | **组件索引(JSON)** | 程序化读取组件信息 |
| `component-cheatsheet.md` | **组件速查表** | 快速查找组件用法 |

---

## 🚀 快速开始

### 1. 查看组件列表
打开 `tuniao-ui-knowledge-base.md` 查看所有组件的分类和基本用法。

### 2. 查找特定组件
- 按功能查找：查看目录分类（基础组件、表单组件、反馈组件等）
- 按名称查找：使用文档内的锚点链接快速跳转
- 按关键词查找：使用编辑器的搜索功能（Cmd/Ctrl + F）

### 3. 学习样式系统
打开 `style-system.md` 学习图鸟UI的完整样式系统，包括：
- 颜色系统（内置颜色、渐变色）
- 尺寸系统（组件尺寸、字体大小）
- 间距系统（padding、margin）
- 布局系统（Flex布局）
- 边框与阴影系统

### 4. 复制代码片段
打开 `quick-reference.md` 获取常用代码片段，直接复制使用。

---

## 📋 组件分类总览

### 🎨 基础组件 (5个)
按钮、图标、标签、头像、徽标

### 📝 表单组件 (14个)
输入框、表单、复选框、单选框、开关、滑动条、步进器、评分、选择器、日期时间选择器、地区选择器、搜索框、软键盘、图片上传

### 💬 反馈组件 (6个)
模态框、操作菜单、弹出框、消息通知、通知栏、遮罩层

### 🧭 导航组件 (3个)
顶部导航栏、底部导航栏、标签栏

### 🎯 展示组件 (14个)
轮播图、标题、线形进度条、圆形进度条、加载图标、加载更多、空白页、步骤条、倒计时、数字跳转、数字滚动、懒加载、相册、瀑布流

### 📐 布局组件 (10个)
列表、吸顶、折叠面板、滑动菜单、分段器、选项卡切换、气泡弹框、横向滚动、索引列表、阅读更多

### 📅 日历组件 (2个)
日历、周日历

### 📄 页面组件 (1个)
页脚

### 🔌 第三方组件
图鸟UI还提供了丰富的第三方扩展组件，包括：
- 悬浮按钮
- 图片裁剪
- 签名板
- 颜色选择器
- 堆叠轮播
- 验证码输入
- 下拉框
- 图文卡片
- 修改用户信息弹框

---

## 🎯 常用组件快速查找

### 我想要...

**实现表单输入** → 使用 `TnForm` + `TnFormItem` + `TnInput`

**显示弹窗提示** → 使用 `TnModal` 或 `TnPopup`

**实现轮播图** → 使用 `TnSwiper`

**实现底部导航** → 使用 `TnTabbar` + `TnTabbarItem`

**实现标签页切换** → 使用 `TnTabs` + `TnTabsItem`

**显示加载状态** → 使用 `TnLoading` 或 `TnLoadmore`

**上传图片** → 使用 `TnImageUpload`

**选择日期** → 使用 `TnCalendar` 或 `TnDateTimePicker`

**显示进度** → 使用 `TnLineProgress` 或 `TnCircleProgress`

**评分功能** → 使用 `TnRate`

**搜索功能** → 使用 `TnSearchBox`

---

## 💡 使用技巧

### 1. 组件引入
```typescript
// 方式一：node方式（推荐）
import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'

// 方式二：uni_modules方式
import TnButton from '@/uni_modules/tuniaoui-vue3/components/button/src/button.vue'
```

### 2. TypeScript支持
```typescript
import type {
  TnModalInstance,
  FormRules,
  LoadmoreStatus,
} from '@tuniao/tnui-vue3-uniapp'
```

### 3. 样式定制
```vue
<!-- 使用内置样式类 -->
<view class="tn-p tn-white_bg tn-radius tn-shadow">内容</view>

<!-- 使用组件属性 -->
<TnButton bg-color="gradient__cool-1" text-color="#fff">按钮</TnButton>

<!-- 使用custom属性 -->
<TnButton custom-class="my-btn" :custom-style="{ fontSize: '32rpx' }">按钮</TnButton>
```

### 4. 事件处理
```vue
<!-- 基础事件 -->
<TnButton @click="handleClick">按钮</TnButton>

<!-- 阻止冒泡 -->
<TnButton click-modifiers="stop" @click="handleClick">按钮</TnButton>

<!-- 表单事件 -->
<TnInput v-model="value" @input="handleInput" @change="handleChange" />
```

---

## 🔍 快速搜索关键词

### 按功能搜索
- **输入**：TnInput, TnSearchBox, TnKeyboard
- **选择**：TnPicker, TnCheckbox, TnRadio, TnSwitch, TnDateTimePicker
- **弹窗**：TnModal, TnPopup, TnActionSheet, TnNotify
- **导航**：TnNavbar, TnTabbar, TnTabs
- **展示**：TnSwiper, TnProgress, TnTag, TnBadge, TnAvatar
- **布局**：TnListItem, TnCollapse, TnWaterFall, TnScrollList
- **加载**：TnLoading, TnLoadmore, TnLazyLoad
- **反馈**：TnNotify, TnNoticeBar, TnOverlay

### 按场景搜索
- **登录注册**：TnForm, TnInput, TnButton
- **商品列表**：TnWaterFall, TnListItem, TnPhotoAlbum
- **购物车**：TnSwipeAction, TnNumberBox, TnCheckbox
- **个人中心**：TnAvatar, TnListItem, TnBadge
- **搜索页面**：TnSearchBox, TnEmpty
- **详情页面**：TnNavbar, TnSwiper, TnReadMore
- **订单页面**：TnSteps, TnCountDown, TnTag

---

## ⚙️ 平台支持

所有组件均支持以下平台：
- ✅ App (vue)
- ✅ H5
- ✅ 微信小程序
- ✅ 支付宝小程序
- 🔄 其他平台适配中

---

## 📖 学习路径

### 新手入门
1. 阅读 `tuniao-ui-knowledge-base.md` 了解组件概览
2. 学习 `style-system.md` 掌握样式系统
3. 参考 `quick-reference.md` 中的代码片段
4. 查阅 `components-detail.md` 了解详细API

### 进阶使用
1. 学习组件组合使用
2. 掌握主题定制方法
3. 了解性能优化技巧
4. 探索第三方扩展组件

---

## 🤝 贡献说明

本知识库基于图鸟UI官方文档整理而成，数据来源：
- 官方文档：https://vue3.tuniaokj.com
- 爬取工具：Firecrawl MCP
- 整理时间：2025-10-27

如发现文档有误或需要更新，请：
1. 访问官方文档获取最新信息
2. 提交Issue或PR
3. 联系维护者更新

---

## 📄 许可证

本知识库仅供学习参考使用，版权归图鸟科技所有。

图鸟UI Vue3使用MIT许可证，详见官方仓库。

---

## 🎓 推荐学习资源

### 官方资源
- [图鸟UI官方文档](https://vue3.tuniaokj.com)
- [图鸟UI GitHub](https://github.com/tuniaoTech/tuniaoui-vue3-uniapp)
- [uni-app官方文档](https://uniapp.dcloud.io)

### 相关技术
- [Vue 3官方文档](https://cn.vuejs.org)
- [TypeScript官方文档](https://www.typescriptlang.org)
- [Vite官方文档](https://vitejs.dev)

---

## 📮 联系方式

- 官方QQ群：[查看官方文档]
- 官方微信：[查看官方文档]
- 官方邮箱：[查看官方文档]

---

**Happy Coding! 🎉**

---

_最后更新：2025-10-27_

