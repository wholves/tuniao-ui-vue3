# 图鸟UI Vue3 GitHub仓库与项目模板

> 📦 基于tuniaoTech组织的官方仓库信息整理  
> 📅 更新时间：2025-10-27  
> 🔗 组织地址：https://github.com/tuniaoTech

## 📚 仓库总览

tuniaoTech组织维护了6个与图鸟UI Vue3相关的仓库，涵盖了源码、演示、模板和插件开发等方面。

| 仓库名 | 类型 | Stars | Forks | 主要语言 | 描述 |
|--------|------|-------|-------|----------|------|
| tuniaoui-rc-vue3-uniapp | 源码 | 342 | 43 | TypeScript 57.1% | 核心组件库源码 |
| tuniaoui-uniapp-v3-demo | 演示 | 66 | 22 | Vue 85.2% | 完整演示项目 |
| tuniaoui-vue3-project-template | 模板 | 1 | 5 | Vue | Vue3项目模板 |
| tuniaoui-vue3-uniapp-template | 模板 | 2 | 11 | Vue | Uniapp Vue3模板 |
| tnuiv3p-graphic-card | 插件 | 2 | 1 | TypeScript 53.3% | 图文卡片组件 |
| tnui-v3-uni-plugin-template | 模板 | 1 | 0 | TypeScript 61.2% | 插件开发模板 |

---

## 1. tuniaoui-rc-vue3-uniapp - 核心源码仓库

### 📦 仓库信息
- **GitHub**: https://github.com/tuniaoTech/tuniaoui-rc-vue3-uniapp
- **Stars**: 342 ⭐
- **Forks**: 43
- **License**: MIT
- **最后更新**: 2024年7月

### 📝 仓库说明
这是图鸟UI Vue3 Uniapp版本的核心源码仓库，包含了所有组件的完整源代码。

### 🎯 主要特性
1. **完整的布局系统**
   - Flex布局
   - Grid布局
   - 浮动布局

2. **丰富的配色体系**
   - 4种色深模式（标准、深色、浅色、禁用）
   - 4套渐变配色方案
   - 100+颜色变量

3. **700+图标库**
   - 风格统一的图标icon
   - 独立的npm包(@tuniao/tn-icon)
   - 便于单独更新

4. **60+精选组件**
   - 基础组件
   - 表单组件
   - 反馈组件
   - 导航组件
   - 展示组件
   - 布局组件

5. **酷炫页面模板**
   - 常用页面模板
   - 眼前一亮的界面效果
   - 多端适配

### 📂 目录结构
```
tuniaoui-rc-vue3-uniapp/
├── components/         # 组件源码
├── constants/          # 常量定义
├── hooks/              # Vue3 Hooks
├── lib/                # 工具库
├── libs/               # 第三方库
├── theme-chalk/        # 样式主题
├── tokens/             # 设计令牌
├── typings/            # TypeScript类型定义
├── utils/              # 工具函数
├── CHANGELOG.md        # 更新日志
├── LICENSE             # MIT许可证
├── README.md           # 说明文档
├── global.d.ts         # 全局类型定义
├── index.ts            # 入口文件
└── package.json        # 包配置
```

### 🔧 技术栈
- TypeScript: 57.1%
- JavaScript: 26.1%
- Vue: 8.7%
- SCSS: 8.1%

### 📚 相关链接
- npm包: https://www.npmjs.com/package/@tuniao/tnui-vue3-uniapp
- 使用文档: https://vue3.tuniaokj.com
- 演示代码: https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo
- 图鸟社区: https://www.yuque.com/tuniao

---

## 2. tuniaoui-uniapp-v3-demo - 官方演示项目

### 📦 仓库信息
- **GitHub**: https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo
- **Stars**: 66 ⭐
- **Forks**: 22
- **License**: MIT
- **最后更新**: 2024年7月

### 📝 仓库说明
这是图鸟UI Vue3的完整演示项目，包含了所有组件的使用示例和常用页面模板。

### 🎯 包含内容
1. **所有组件演示页面**
   - 56个核心组件的完整演示
   - 每个组件的多种用法示例
   - 实际应用场景展示

2. **页面模板**
   - 登录注册页面
   - 个人中心页面
   - 商品列表页面
   - 商品详情页面
   - 购物车页面
   - 订单页面
   - 搜索页面
   - 表单页面

3. **最佳实践示例**
   - 组件组合使用
   - 表单验证
   - 状态管理
   - 路由配置

### 📂 项目结构
```
tuniaoui-uniapp-v3-demo/
├── src/
│   ├── pages/          # 页面文件
│   │   ├── index/      # 首页
│   │   ├── component/  # 组件演示
│   │   └── template/   # 页面模板
│   ├── static/         # 静态资源
│   ├── components/     # 自定义组件
│   ├── utils/          # 工具函数
│   ├── App.vue         # 应用入口
│   └── main.ts         # 主入口文件
├── .hbuilderx/         # HBuilderX配置
├── .editorconfig       # 编辑器配置
├── .eslintrc.json      # ESLint配置
├── .prettierrc         # Prettier配置
├── index.html          # H5入口
├── package.json        # 依赖配置
├── tsconfig.json       # TypeScript配置
└── vite.config.ts      # Vite配置
```

### 🔧 技术栈
- Vue: 85.2%
- SCSS: 8.7%
- TypeScript: 6.0%
- HTML: 0.1%

### 🚀 快速开始
```bash
# 克隆项目
git clone https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo.git

# 安装依赖
cd tuniaoui-uniapp-v3-demo
pnpm install

# 运行微信小程序
pnpm dev:mp-weixin

# 运行H5
pnpm dev:h5

# 运行App
pnpm dev:app
```

### 💡 学习建议
1. **第一步**: 运行演示项目，体验所有组件
2. **第二步**: 查看组件演示页面源码，学习用法
3. **第三步**: 参考页面模板，构建自己的页面
4. **第四步**: 深入研究源码，理解实现原理

---

## 3. tuniaoui-vue3-project-template - Vue3项目模板

### 📦 仓库信息
- **GitHub**: https://github.com/tuniaoTech/tuniaoui-vue3-project-template
- **Stars**: 1 ⭐
- **Forks**: 5
- **最后更新**: 2024年1月

### 📝 仓库说明
这是图鸟UI Vue3的项目模板，适用于快速创建新项目。

### 🎯 适用场景
- 快速创建新项目
- 标准化项目结构
- 预配置开发环境

### 💡 使用方式
```bash
# 使用GitHub模板创建新项目
# 1. 访问仓库页面
# 2. 点击 "Use this template" 按钮
# 3. 创建自己的仓库

# 或者直接克隆
git clone https://github.com/tuniaoTech/tuniaoui-vue3-project-template.git my-project
cd my-project
npm install
```

---

## 4. tuniaoui-vue3-uniapp-template - Uniapp Vue3模板

### 📦 仓库信息
- **GitHub**: https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template
- **Stars**: 2 ⭐
- **Forks**: 11
- **最后更新**: 2024年1月

### 📝 仓库说明
这是图鸟UI Uniapp Vue3的标准模板，由tuniao-cli工具使用。

### 🎯 主要用途
1. **CLI工具使用**
   - tuniao-cli默认模板
   - 快速项目初始化
   - 开箱即用

2. **手动克隆使用**
   - 直接克隆到本地
   - 自定义项目名称
   - 独立开发

### 💡 使用方式

#### 方式1: 使用CLI (推荐)
```bash
# 安装CLI工具
npm install -g tuniao-cli

# 使用CLI创建项目（会自动使用此模板）
tuniao create my-project
```

#### 方式2: 手动克隆
```bash
# 克隆模板
git clone https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template.git my-project

# 或从Gitee克隆（国内更快）
git clone https://gitee.com/TSpecific/tuniao-ui-vue3-uniapp-template my-project

# 安装依赖
cd my-project
npm install

# 运行项目
npm run dev:mp-weixin
```

### 📦 包含内容
- ✅ 完整的项目结构
- ✅ 预配置的开发环境
- ✅ TuniaoUI集成配置
- ✅ TypeScript支持
- ✅ ESLint + Prettier
- ✅ Vite配置
- ✅ 基础页面示例

---

## 5. tnuiv3p-graphic-card - 图文卡片组件

### 📦 仓库信息
- **GitHub**: https://github.com/tuniaoTech/tnuiv3p-graphic-card
- **npm**: tnuiv3p-tn-graphic-card
- **Stars**: 2 ⭐
- **Forks**: 1
- **最后更新**: 2023年11月

### 📝 组件说明
图文卡片组件，用于展示图文简要信息，让用户快速查看筛选数据。常用于社交应用、资讯应用的内容展示。

### 🎯 主要功能
- ✅ 显示作者头像和信息
- ✅ 显示标题和描述
- ✅ 显示内容标签
- ✅ 显示文章内容预览
- ✅ 显示图片列表（最多9张）
- ✅ 显示热度、评论、点赞数量
- ✅ 显示浏览用户头像

### 📦 安装使用

#### 安装
```bash
npm install tnuiv3p-tn-graphic-card
```

#### 引入
```typescript
import TnGraphicCard from 'tnuiv3p-tn-graphic-card/index.vue'
```

#### 基本用法
```vue
<script setup lang="ts">
const graphicData = {
  id: 1,
  avatar: 'https://tnuiimage.tnkjapp.com/avatar/normal/1.png',
  title: '文章标题',
  description: '2023年6月30日',
  tags: ['标签1', '标签2'],
  content: '文章简要内容...',
  images: [
    'https://tnuiimage.tnkjapp.com/swiper/ad1.jpg',
    'https://tnuiimage.tnkjapp.com/swiper/ad2.jpg',
    'https://tnuiimage.tnkjapp.com/swiper/ad3.jpg',
  ],
  viewCount: 100,
  commentCount: 10,
  likeCount: 20,
  viewUserAvatars: [
    'https://tnuiimage.tnkjapp.com/avatar/normal/1.png',
    'https://tnuiimage.tnkjapp.com/avatar/normal/2.png',
  ],
}
</script>

<template>
  <TnGraphicCard
    :avatar="graphicData.avatar"
    :title="graphicData.title"
    :description="graphicData.description"
    :tags="graphicData.tags"
    :content="graphicData.content"
    :images="graphicData.images"
    :view-count="graphicData.viewCount"
    :comment-count="graphicData.commentCount"
    :like-count="graphicData.likeCount"
    :view-user-avatars="graphicData.viewUserAvatars"
  />
</template>
```

### Props详解

| 属性名 | 说明 | 类型 | 必填 |
|--------|------|------|------|
| avatar | 发布者头像地址 | String | ✅ 是 |
| title | 标题 | String | ✅ 是 |
| description | 描述 | String | ✅ 是 |
| content | 内容 | String | 否 |
| tags | 标签数组 | String[] | 否 |
| images | 图片列表 | String[] | 否 |
| tag-bg-color | 标签背景色 | String | 否 |
| tag-text-color | 标签文字色 | String | 否 |
| show-more | 显示更多按钮 | Boolean | 否 |
| show-hot | 显示热度 | Boolean | 否 |
| active-hot | 激活热度 | Boolean | 否 |
| hot-count | 热度数量 | Number | 否 |
| hot-icon | 热度图标 | String | 否 |
| show-comment | 显示评论 | Boolean | 否 |
| active-comment | 激活评论 | Boolean | 否 |
| comment-count | 评论数量 | Number | 否 |
| show-like | 显示点赞 | Boolean | 否 |
| active-like | 激活点赞 | Boolean | 否 |
| like-count | 点赞数量 | Number | 否 |
| show-view-user | 显示查看用户 | Boolean | 否 |
| view-count | 实际查看数 | Number | 否 |
| view-user-avatars | 查看用户头像列表 | String[] | 否 |
| max-view-user-avatar-count | 最大显示头像数 | Number | 否 |

### Events

| 事件名 | 说明 | 类型 |
|--------|------|------|
| click | 图文卡片点击 | () => void |
| avatar-view-click | 头像和查看数点击 | () => void |
| more-click | 更多按钮点击 | () => void |
| hot-click | 热度点击 | () => void |
| comment-click | 评论点击 | () => void |
| like-click | 点赞点击 | () => void |

### Slots

| 插槽名 | 说明 |
|--------|------|
| briefOperation | 顶部右边操作区域 |
| bottomRight | 底部右边操作区域 |

### 使用示例

#### 示例1: 基础图文卡片
```vue
<TnGraphicCard
  avatar="https://tnuiimage.tnkjapp.com/avatar/normal/1.png"
  title="图鸟UI发布新版本啦"
  description="2024年7月18日"
  :tags="['Vue3', 'Uniapp', 'TypeScript']"
  content="图鸟UI Vue3最新版本已经发布，修复了多个bug，新增了多个实用功能..."
  :images="['img1.jpg', 'img2.jpg']"
  :view-count="1234"
  :comment-count="56"
  :like-count="789"
/>
```

#### 示例2: 隐藏查看数并设置为已点赞
```vue
<TnGraphicCard
  avatar="..."
  title="..."
  description="..."
  :show-view="false"
  active-like
  :like-count="100"
/>
```

#### 示例3: 限制显示浏览用户头像数量
```vue
<TnGraphicCard
  avatar="..."
  title="..."
  description="..."
  :view-user-avatars="avatarList"
  :max-view-user-avatar-count="3"
/>
```

---

## 6. tnui-v3-uni-plugin-template - 插件开发模板

### 📦 仓库信息
- **GitHub**: https://github.com/tuniaoTech/tnui-v3-uni-plugin-template
- **Stars**: 1 ⭐
- **最后更新**: 2023年9月

### 📝 仓库说明
这是图鸟UI Vue3 Uniapp插件的开发模板，用于快速创建第三方组件。

### 🎯 适用场景
- 开发图鸟UI第三方组件
- 贡献开源组件
- 学习组件开发

### 📂 模板结构
```
tnui-v3-uni-plugin-template/
├── internal/           # 内部配置
├── play/               # 演示playground
├── scripts/            # 构建脚本
├── .editorconfig       # 编辑器配置
├── .env                # 环境变量
├── .eslintrc.json      # ESLint配置
├── .prettierrc         # Prettier配置
├── CHANGELOG.md        # 更新日志模板
├── LICENSE             # MIT许可证
├── README.md           # 文档模板
├── package.json        # 包配置
├── tsconfig.*.json     # TypeScript配置
└── pnpm-workspace.yaml # pnpm工作区配置
```

### 🔧 技术栈
- TypeScript: 61.2%
- SCSS: 27.8%
- Vue: 4.0%
- Shell: 3.7%
- HTML: 3.3%

### 💡 开发流程
1. **克隆模板**
```bash
git clone https://github.com/tuniaoTech/tnui-v3-uni-plugin-template.git my-component
cd my-component
```

2. **修改配置**
   - 修改package.json中的组件名称
   - 修改README.md文档
   - 开发组件功能

3. **本地测试**
```bash
pnpm install
pnpm dev  # 启动playground测试
```

4. **发布组件**
```bash
pnpm build
npm publish
```

5. **联系官方收录**
   - 微信: tnkewo
   - 备注: tuniaoUI vue3 插件开发

---

## 🌟 项目特性总结

### 共同特性
所有图鸟UI相关项目都具有以下特性：

1. **技术栈统一**
   - Vue 3
   - TypeScript
   - Uniapp
   - Vite

2. **代码规范**
   - ESLint代码检查
   - Prettier代码格式化
   - EditorConfig编辑器配置

3. **多端支持**
   - 微信小程序
   - 支付宝小程序
   - H5
   - App

4. **MIT开源**
   - 自由使用
   - 可商用
   - 可修改

---

## 📖 使用建议

### 新手开发者
1. **从演示项目开始**
   ```bash
   git clone https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo.git
   cd tuniaoui-uniapp-v3-demo
   pnpm install
   pnpm dev:mp-weixin
   ```

2. **运行查看所有组件**
   - 了解组件功能
   - 学习使用方法
   - 参考代码示例

3. **创建自己的项目**
   ```bash
   npm install -g tuniao-cli
   tuniao create my-project
   ```

### 有经验开发者
1. **直接使用模板**
   - 使用tuniaoui-vue3-uniapp-template
   - 快速搭建项目骨架

2. **参考源码**
   - 查看tuniaoui-rc-vue3-uniapp源码
   - 深入理解实现原理

3. **开发第三方组件**
   - 使用tnui-v3-uni-plugin-template
   - 贡献开源生态

---

## 🔗 资源链接汇总

### 官方仓库
| 仓库 | 链接 |
|------|------|
| 核心源码 | https://github.com/tuniaoTech/tuniaoui-rc-vue3-uniapp |
| 演示项目 | https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo |
| Vue3项目模板 | https://github.com/tuniaoTech/tuniaoui-vue3-project-template |
| Uniapp模板 | https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template |
| 图文卡片组件 | https://github.com/tuniaoTech/tnuiv3p-graphic-card |
| 插件开发模板 | https://github.com/tuniaoTech/tnui-v3-uni-plugin-template |

### 镜像地址
| 平台 | Uniapp模板链接 |
|------|---------------|
| GitHub | https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template |
| Gitee | https://gitee.com/TSpecific/tuniao-ui-vue3-uniapp-template |

### 其他资源
- 官方文档: https://vue3.tuniaokj.com
- npm包: https://www.npmjs.com/package/@tuniao/tnui-vue3-uniapp
- 图鸟社区: https://www.yuque.com/tuniao
- 插件市场: https://ext.dcloud.net.cn/plugin?id=13530

---

## 👥 社区与联系

### 作者联系方式
- **微信**: tnkewo
- **GitHub**: https://github.com/tuniaoTech

### 加入社区
扫码加入图鸟UI技术交流群：

![扫码进群](https://resource.tuniaokj.com/images/about_tuniao/tn_author_qrcode.jpg)

**群特色**：
- 💬 专注技术交流
- 🎯 专业的前端群
- 🤝 良好的氛围
- 📚 及时的问题解答

### 贡献代码
欢迎提交PR贡献代码：
1. Fork仓库
2. 创建分支
3. 提交代码
4. 发起Pull Request

---

## 📊 仓库统计对比

### 活跃度对比
| 仓库 | Stars | Forks | 最后更新 | 活跃度 |
|------|-------|-------|----------|--------|
| tuniaoui-rc-vue3-uniapp | 342 | 43 | 2024-07 | ⭐⭐⭐⭐⭐ |
| tuniaoui-uniapp-v3-demo | 66 | 22 | 2024-07 | ⭐⭐⭐⭐ |
| tuniaoui-vue3-uniapp-template | 2 | 11 | 2024-01 | ⭐⭐⭐ |
| tuniaoui-vue3-project-template | 1 | 5 | 2024-01 | ⭐⭐ |
| tnuiv3p-graphic-card | 2 | 1 | 2023-11 | ⭐⭐ |
| tnui-v3-uni-plugin-template | 1 | 0 | 2023-09 | ⭐ |

### 语言分布
| 仓库 | 主要语言 | 占比 |
|------|----------|------|
| tuniaoui-rc-vue3-uniapp | TypeScript | 57.1% |
| tuniaoui-uniapp-v3-demo | Vue | 85.2% |
| tnuiv3p-graphic-card | TypeScript | 53.3% |
| tnui-v3-uni-plugin-template | TypeScript | 61.2% |

---

## 🎨 项目Banner

所有官方项目都使用统一的Banner图片：

**Vue3 Banner**:
```
https://resource.tuniaokj.com/images/vue3/market/vue3-banner-min.jpg
```

**Vue3 Code**:
```
https://resource.tuniaokj.com/images/vue3/market/vue3-code-min.jpg
```

---

## 💻 开发环境要求

### 基础要求
- Node.js >= 16.0.0
- pnpm >= 7.0.0 (推荐) 或 npm >= 8.0.0
- Git

### IDE推荐
- VSCode + Volar (推荐)
- HBuilderX (uni_modules方式)

### 插件推荐
- Vue Language Features (Volar)
- TypeScript Vue Plugin (Volar)
- ESLint
- Prettier
- uni-helper

---

## 🎯 选择合适的起点

### 我想快速开始开发
✅ 使用 **tuniao-cli**
```bash
npm install -g tuniao-cli
tuniao create my-project
```

### 我想学习图鸟UI
✅ 克隆 **演示项目**
```bash
git clone https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo.git
```

### 我想从模板开始
✅ 使用 **项目模板**
```bash
git clone https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template.git
```

### 我想查看源码
✅ 查看 **源码仓库**
```bash
git clone https://github.com/tuniaoTech/tuniaoui-rc-vue3-uniapp.git
```

### 我想开发插件
✅ 使用 **插件模板**
```bash
git clone https://github.com/tuniaoTech/tnui-v3-uni-plugin-template.git
```

---

## 📚 最佳实践

### 1. 项目初始化
```bash
# 推荐使用pnpm
npm install -g pnpm

# 使用CLI创建项目
npm install -g tuniao-cli
tuniao create my-project

# 进入项目
cd my-project

# 安装依赖
pnpm install
```

### 2. 开发规范
- ✅ 使用TypeScript编写代码
- ✅ 遵循ESLint规则
- ✅ 使用Prettier格式化代码
- ✅ 编写详细的注释
- ✅ 提交前进行类型检查

### 3. 组件使用
```vue
<script setup lang="ts">
// 导入组件
import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'
// 导入类型
import type { TnButtonInstance } from '@tuniao/tnui-vue3-uniapp'
</script>

<template>
  <TnButton type="primary">按钮</TnButton>
</template>
```

### 4. 样式使用
```vue
<template>
  <view class="tn-p tn-white_bg tn-radius tn-shadow">
    内容
  </view>
</template>

<style lang="scss">
// 可以使用图鸟UI的scss变量
.custom-class {
  color: var(--tn-color-primary);
  padding: var(--tn-spacing);
}
</style>
```

---

## 🔄 项目维护

### 更新频率
根据GitHub提交记录：
- **源码仓库**: 定期更新，修复bug和添加新功能
- **演示项目**: 跟随源码更新
- **模板项目**: 不定期更新

### 获取最新版本
```bash
# 查看当前版本
npm list @tuniao/tnui-vue3-uniapp

# 更新到最新版本
npm update @tuniao/tnui-vue3-uniapp @tuniao/tn-icon @tuniao/tn-style
```

### 查看更新日志
- GitHub仓库的CHANGELOG.md
- 官方文档: https://vue3.tuniaokj.com/doc/guide/changelog.html

---

## 🎓 学习路径

### Level 1: 入门阶段
1. 克隆演示项目运行查看
2. 浏览所有组件演示
3. 理解项目结构
4. 学习基础组件使用

### Level 2: 实践阶段
1. 使用CLI创建自己的项目
2. 参考演示项目实现页面
3. 学习组件组合使用
4. 掌握样式系统

### Level 3: 进阶阶段
1. 查看源码理解实现
2. 学习TypeScript类型系统
3. 了解Hooks使用
4. 掌握最佳实践

### Level 4: 贡献阶段
1. 发现并报告bug
2. 提交PR修复问题
3. 开发第三方组件
4. 帮助其他开发者

---

## 🎉 总结

tuniaoTech组织提供了完整的图鸟UI生态：

1. **核心源码** - 高质量的组件库
2. **演示项目** - 完整的使用示例
3. **项目模板** - 快速开始开发
4. **开发工具** - CLI命令行工具
5. **插件模板** - 扩展组件开发
6. **活跃社区** - 技术交流支持

**GitHub统计**：
- 总Stars: 400+
- 总Forks: 80+
- 活跃维护
- 持续更新

**推荐资源**：
- ⭐⭐⭐⭐⭐ 演示项目 (学习)
- ⭐⭐⭐⭐⭐ 项目模板 (开发)
- ⭐⭐⭐⭐ 源码仓库 (研究)
- ⭐⭐⭐ 插件模板 (扩展)

---

**开始使用图鸟UI，快速构建美观的跨平台应用！** 🚀

---

_数据来源：GitHub tuniaoTech组织_  
_更新时间：2025-10-27_  
_整理者：wholves_

