# 图鸟UI Vue3 安装指南

> 📦 TuniaoUI Vue3 Typescript Uniapp版本安装教程  
> 📅 更新时间：2025-10-27

## 📖 简介

TuniaoUI是一个基于uni-app开发的跨平台Vue3组件库，使用TypeScript编写，提供丰富的UI组件和完善的类型支持。

### 特点
- ✅ Vue3 + TypeScript
- ✅ 跨平台支持（App、H5、微信小程序、支付宝小程序等）
- ✅ 丰富的组件库（56+核心组件）
- ✅ 第三方组件生态
- ✅ MIT开源协议
- ✅ 完善的文档

### 开源协议
TuniaoUI vue3 Typescript开源组件遵循MIT协议，开发者可以自由的享受和参与开源。

**⚠️ 注意**：这并不意味着您可以将TuniaoUI应用到非法的领域，比如涉及赌博，暴力等方面。如因此产生纠纷等法律问题，图鸟不承担任何责任。

---

## 🚀 安装方式

TuniaoUI提供了三种安装方式，推荐使用tuniao-cli方式创建项目。

### 方式一：tuniao-cli 方式（推荐）

这是最简单快捷的方式，可以一键创建包含TuniaoUI的项目模板。

#### 1. 安装tuniao-cli

**前置要求**：
- ✅ 已安装 Node.js（建议v16+）
- ✅ 已安装 Git
- ✅ 已配置好环境变量

**安装命令**：
```bash
# npm
npm install tuniao-cli -g

# pnpm (推荐)
pnpm install tuniao-cli -g

# yarn
yarn add tuniao-cli -g
```

#### 2. 创建项目

```bash
# 创建项目（会创建新文件夹）
tuniao create my-project

# 或者在当前目录创建
tuniao create
```

#### 3. 根据提示选择配置

创建项目时会有交互式提示，按需选择：
- 项目名称
- 是否使用TypeScript
- 是否使用Pinia状态管理
- 是否使用uni-ui
- 等等...

#### 4. 安装依赖并运行

```bash
cd my-project
npm install
npm run dev:mp-weixin  # 微信小程序
npm run dev:h5         # H5
npm run dev:app        # App
```

#### ⚠️ Windows用户注意

如果在Windows下使用tuniao-cli创建项目时提示：
```
无法加载文件...因为在此系统上禁止运行脚本
```

请在**管理员模式**下打开PowerShell，执行以下命令：
```bash
set-ExecutionPolicy RemoteSigned
```

#### 模板地址

如果下载模板过慢，可以直接从GitHub或Gitee克隆模板：

**GitHub**：
```bash
git clone https://github.com/tuniaoTech/tuniaoui-vue3-uniapp-template
```

**Gitee**：
```bash
git clone https://gitee.com/TSpecific/tuniao-ui-vue3-uniapp-template
```

---

### 方式二：Node方式安装

适合已有uni-app项目，想要集成TuniaoUI的情况。

#### 1. 安装核心包

由于TuniaoUI以源码方式发布，需要同时安装依赖包：

```bash
# npm
npm install @tuniao/tnui-vue3-uniapp @tuniao/tn-icon @tuniao/tn-style

# pnpm (推荐)
pnpm add @tuniao/tnui-vue3-uniapp @tuniao/tn-icon @tuniao/tn-style

# yarn
yarn add @tuniao/tnui-vue3-uniapp @tuniao/tn-icon @tuniao/tn-style
```

#### 2. 安装Sass环境

TuniaoUI使用Sass进行开发，需要安装Sass环境：

```bash
# npm
npm install sass sass-loader -D

# pnpm
pnpm install sass sass-loader -D

# yarn
yarn add sass sass-loader -D
```

#### 3. 项目配置

安装完成后需要进行项目配置，详见 [项目配置](#项目配置)

---

### 方式三：uni_modules方式安装

适合使用HBuilderX开发的用户。

#### 1. 访问插件市场

访问uniapp插件市场：  
https://ext.dcloud.net.cn/plugin?name=tuniaoui-vue3

#### 2. 导入插件

点击"使用HBuilderX导入插件"或"下载插件ZIP"

#### 3. 项目配置

导入后需要进行项目配置，详见 [项目配置](#项目配置)

---

## ⚙️ 项目配置

### Node方式安装配置

#### 1. 配置vite.config.ts

在项目根目录的`vite.config.ts`中添加以下配置：

```typescript
import { defineConfig } from 'vite'
import uni from '@dcloudio/vite-plugin-uni'

export default defineConfig({
  plugins: [uni()],
  css: {
    preprocessorOptions: {
      scss: {
        additionalData: `
          @import "@tuniao/tn-style/index.scss";
        `
      }
    }
  }
})
```

#### 2. 配置tsconfig.json

在`tsconfig.json`中添加类型声明：

```json
{
  "compilerOptions": {
    "types": [
      "@dcloudio/types",
      "@tuniao/tnui-vue3-uniapp"
    ]
  }
}
```

#### 3. 引入图标样式

在`App.vue`或`main.ts`中引入图标样式：

```vue
<style>
@import '@tuniao/tn-icon/dist/index.css';
</style>
```

或者在`main.ts`中：

```typescript
import '@tuniao/tn-icon/dist/index.css'
```

### uni_modules方式安装配置

#### 1. 配置pages.json

在`pages.json`中添加easycom规则：

```json
{
  "easycom": {
    "autoscan": true,
    "custom": {
      "^tn-(.*)": "@/uni_modules/tuniaoui-vue3/components/$1/src/$1.vue"
    }
  }
}
```

#### 2. 配置uni.scss

在`uni.scss`中引入样式：

```scss
@import '@/uni_modules/tuniaoui-vue3/theme/index.scss';
```

---

## 📱 平台支持

| 平台 | 支持情况 | 说明 |
|------|---------|------|
| App (vue) | ✅ 完全支持 | - |
| H5 | ✅ 完全支持 | - |
| 微信小程序 | ✅ 完全支持 | - |
| 支付宝小程序 | ✅ 完全支持 | - |
| 百度小程序 | 🔄 适配中 | - |
| 字节跳动小程序 | 🔄 适配中 | - |
| QQ小程序 | 🔄 适配中 | - |

---

## 🎨 演示项目

### 微信小程序演示

扫描二维码体验（请查看官方文档）

### 支付宝小程序演示

扫描二维码体验（请查看官方文档）

### 源码地址

#### CLI方式创建的示例项目
GitHub：https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo

#### uni_modules方式示例
插件市场：https://ext.dcloud.net.cn/plugin?id=13530

---

## 🔧 开发环境要求

### 推荐配置
- Node.js >= 16.0.0
- pnpm >= 7.0.0 (或npm >= 8.0.0)
- Vue >= 3.2.0
- TypeScript >= 4.5.0
- HBuilderX >= 3.6.0 (使用uni_modules方式)

### IDE推荐
- **VSCode** + Volar (推荐)
- **HBuilderX** (uni_modules方式)

### VSCode插件推荐
- Vue Language Features (Volar)
- TypeScript Vue Plugin (Volar)
- uni-helper
- ESLint
- Prettier

---

## 📦 包说明

### 核心包

#### @tuniao/tnui-vue3-uniapp
- **说明**：TuniaoUI核心组件库
- **版本**：查看 [npm](https://www.npmjs.com/package/@tuniao/tnui-vue3-uniapp)
- **大小**：约2MB（源码）
- **包含**：所有核心UI组件

#### @tuniao/tn-icon
- **说明**：图鸟图标字体库
- **版本**：查看 [npm](https://www.npmjs.com/package/@tuniao/tn-icon)
- **包含**：完整的图标字体文件

#### @tuniao/tn-style
- **说明**：图鸟样式系统
- **版本**：查看 [npm](https://www.npmjs.com/package/@tuniao/tn-style)
- **包含**：颜色、间距、布局等样式

### 第三方扩展包

所有第三方组件包名格式：`tnuiv3p-tn-<component-name>`

示例：
- `tnuiv3p-tn-suspend-button` - 悬浮按钮
- `tnuiv3p-tn-image-crop` - 图片裁剪
- `tnuiv3p-tn-sign-board` - 签名板

---

## 🎯 快速开始

### 1. 创建项目

```bash
# 安装CLI
npm install tuniao-cli -g

# 创建项目
tuniao create my-tuniao-project

# 进入项目
cd my-tuniao-project

# 安装依赖
npm install
```

### 2. 运行项目

```bash
# 微信小程序
npm run dev:mp-weixin

# H5
npm run dev:h5

# App
npm run dev:app
```

### 3. 开始使用组件

```vue
<script setup lang="ts">
import { ref } from 'vue'
import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'

const count = ref(0)
</script>

<template>
  <view class="container">
    <TnButton type="primary" @click="count++">
      点击了{{ count }}次
    </TnButton>
  </view>
</template>

<style lang="scss" scoped>
.container {
  padding: 30rpx;
}
</style>
```

---

## 🆘 常见问题

### Q1: 安装后提示找不到模块？

**原因**：没有正确配置tsconfig.json或vite.config.ts

**解决**：
1. 检查`tsconfig.json`中是否添加了类型声明
2. 检查`vite.config.ts`中是否配置了scss
3. 重启开发服务器

### Q2: 样式不生效？

**原因**：没有引入样式文件

**解决**：
1. 检查是否引入了`@tuniao/tn-icon/dist/index.css`
2. 检查`vite.config.ts`中的scss配置
3. 确保组件路径正确

### Q3: TypeScript类型错误？

**原因**：类型声明配置不正确

**解决**：
```json
// tsconfig.json
{
  "compilerOptions": {
    "types": [
      "@dcloudio/types",
      "@tuniao/tnui-vue3-uniapp"
    ]
  }
}
```

### Q4: 第三方组件安装后无法使用？

**原因**：第三方组件只支持特定方式创建的项目

**解决**：
- 使用`tuniao-cli`创建项目
- 或使用node方式安装TuniaoUI
- uni_modules方式暂不支持第三方组件

### Q5: Windows下无法运行tuniao-cli？

**原因**：PowerShell执行策略限制

**解决**：
管理员模式打开PowerShell，执行：
```bash
set-ExecutionPolicy RemoteSigned
```

---

## 🔄 更新指南

### 更新核心组件库

```bash
# npm
npm update @tuniao/tnui-vue3-uniapp @tuniao/tn-icon @tuniao/tn-style

# pnpm
pnpm update @tuniao/tnui-vue3-uniapp @tuniao/tn-icon @tuniao/tn-style

# yarn
yarn upgrade @tuniao/tnui-vue3-uniapp @tuniao/tn-icon @tuniao/tn-style
```

### 更新第三方组件

```bash
# 更新单个组件
npm update tnuiv3p-tn-suspend-button

# 更新所有tnuiv3p开头的包
npm update $(npm list --depth=0 | grep tnuiv3p | awk '{print $2}' | cut -d@ -f1)
```

### 查看版本信息

```bash
# 查看已安装版本
npm list @tuniao/tnui-vue3-uniapp

# 查看可用版本
npm view @tuniao/tnui-vue3-uniapp versions
```

---

## 📚 相关资源

### 官方资源
- 📖 官方文档：https://vue3.tuniaokj.com
- 💻 GitHub仓库：https://github.com/tuniaoTech/tuniaoui-rc-vue3-uniapp
- 📦 npm包：https://www.npmjs.com/package/@tuniao/tnui-vue3-uniapp
- 🎨 图标库：https://www.npmjs.com/package/@tuniao/tn-icon
- 🔧 CLI工具：https://www.npmjs.com/package/tuniao-cli

### 示例项目
- CLI示例：https://github.com/tuniaoTech/tuniaoui-uniapp-v3-demo
- uni_modules示例：https://ext.dcloud.net.cn/plugin?id=13530

### 技术栈
- uni-app：https://uniapp.dcloud.io
- Vue3：https://cn.vuejs.org
- TypeScript：https://www.typescriptlang.org
- Vite：https://vitejs.dev

---

## 👥 贡献者

感谢以下开发者的贡献（不分先后）：
- [北笙༊](https://github.com/abdukuddus)
- [孟夏乾月](https://github.com/cathcy8869)
- [FelixL-Dev](https://github.com/FelixL-Dev)

---

## 📞 技术支持

### 官方联系方式
- 微信：tnkewo（第三方组件开发）
- GitHub Issues：提交bug和建议
- 官方文档：查看最新文档

### 社区
- QQ群：查看官方文档
- 微信群：查看官方文档
- 论坛：查看官方文档

---

## 🎓 下一步

安装完成后，建议：
1. ✅ 阅读 [快速开始](#快速开始) 了解基本用法
2. ✅ 查看 [组件文档](./tuniao-ui-knowledge-base.md) 了解所有组件
3. ✅ 学习 [样式系统](./style-system.md) 掌握样式使用
4. ✅ 参考 [代码示例](./quick-reference.md) 快速开发

---

## 📝 版本说明

### 当前版本
- **TuniaoUI Vue3**：查看 [npm版本](https://www.npmjs.com/package/@tuniao/tnui-vue3-uniapp)
- **图鸟图标**：查看 [npm版本](https://www.npmjs.com/package/@tuniao/tn-icon)

### Vue2版本
如果需要使用Vue2版本，请访问：https://vue2.tuniaokj.com/

### 更新日志
查看官方文档了解详细更新日志：https://vue3.tuniaokj.com/doc/guide/changelog.html

---

## 🌟 推荐配置

### package.json示例

```json
{
  "name": "my-tuniao-project",
  "version": "1.0.0",
  "scripts": {
    "dev:mp-weixin": "uni -p mp-weixin",
    "dev:h5": "uni",
    "build:mp-weixin": "uni build -p mp-weixin",
    "build:h5": "uni build"
  },
  "dependencies": {
    "@dcloudio/uni-app": "^3.0.0",
    "@tuniao/tnui-vue3-uniapp": "latest",
    "@tuniao/tn-icon": "latest",
    "@tuniao/tn-style": "latest",
    "vue": "^3.2.0"
  },
  "devDependencies": {
    "@dcloudio/types": "^3.0.0",
    "@dcloudio/vite-plugin-uni": "^3.0.0",
    "sass": "^1.60.0",
    "sass-loader": "^13.0.0",
    "typescript": "^4.9.0",
    "vite": "^4.0.0"
  }
}
```

### tsconfig.json示例

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

### vite.config.ts示例

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

---

## ✅ 验证安装

安装完成后，创建一个测试页面验证是否安装成功：

```vue
<script setup lang="ts">
import { ref } from 'vue'
import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'
import TnIcon from '@tuniao/tnui-vue3-uniapp/components/icon/src/icon.vue'

const count = ref(0)
</script>

<template>
  <view class="container tn-p">
    <view class="tn-mb tn-flex-center">
      <TnIcon name="logo-tuniao" size="100" color="tn-blue" />
    </view>
    
    <view class="tn-mb tn-text-center">
      <text class="tn-text-xl tn-text-bold">TuniaoUI Vue3</text>
    </view>
    
    <view class="tn-mb tn-flex-center">
      <text>当前计数：{{ count }}</text>
    </view>
    
    <view class="tn-flex-center">
      <TnButton type="primary" @click="count++">
        点击+1
      </TnButton>
    </view>
  </view>
</template>

<style lang="scss" scoped>
.container {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
```

如果页面正常显示且功能正常，说明安装成功！🎉

---

## 🚨 故障排除

### 问题1：安装时报错

**可能原因**：
- 网络问题
- npm源配置问题
- Node版本过低

**解决方案**：
```bash
# 切换npm源到淘宝源
npm config set registry https://registry.npmmirror.com

# 或使用nrm管理源
npm install -g nrm
nrm use taobao

# 升级Node版本
# 访问 https://nodejs.org 下载最新LTS版本
```

### 问题2：编译时报错

**可能原因**：
- TypeScript配置问题
- Sass环境问题
- 路径配置问题

**解决方案**：
1. 检查tsconfig.json配置
2. 确保已安装sass和sass-loader
3. 检查vite.config.ts中的路径配置
4. 清除缓存重新编译

```bash
# 清除缓存
rm -rf node_modules
rm -rf .hbuilderx
rm package-lock.json

# 重新安装
npm install
```

### 问题3：组件样式丢失

**可能原因**：
- 样式文件未引入
- scss配置错误

**解决方案**：
1. 检查是否引入了图标样式
2. 检查vite.config.ts中的scss配置
3. 确保@import路径正确

---

## 📖 推荐学习路径

### 第一天：环境搭建
1. ✅ 安装开发环境
2. ✅ 创建第一个项目
3. ✅ 运行示例项目
4. ✅ 了解项目结构

### 第二天：基础组件
1. ✅ 学习Button、Icon、Tag等基础组件
2. ✅ 掌握样式系统基础
3. ✅ 完成简单页面

### 第三天：表单组件
1. ✅ 学习Input、Form等表单组件
2. ✅ 掌握表单验证
3. ✅ 完成登录注册页面

### 第四天：反馈与导航
1. ✅ 学习弹窗、导航组件
2. ✅ 完成完整应用框架

---

祝您使用愉快！🎉

如有问题，请查阅官方文档或提Issue：https://github.com/tuniaoTech/tuniaoui-rc-vue3-uniapp/issues

