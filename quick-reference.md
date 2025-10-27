# 图鸟UI Vue3 快速参考手册

## 快速开始

### 安装
```bash
# 使用tuniao-cli创建项目
npm install -g @tuniao/cli
tuniao create my-project

# 或者手动安装
npm install @tuniao/tnui-vue3-uniapp
```

### 引入方式

#### 方式一：node方式
```typescript
import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'
```

#### 方式二：uni_modules方式
```typescript
import TnButton from '@/uni_modules/tuniaoui-vue3/components/button/src/button.vue'
```

---

## 组件快速查询

### 按使用场景分类

#### 📝 表单输入
| 组件 | 使用场景 | 快速示例 |
|------|----------|----------|
| TnInput | 文本输入 | `<TnInput v-model="value" placeholder="请输入" />` |
| TnCheckbox | 多选 | `<TnCheckbox v-model="checked" label="选项">选项</TnCheckbox>` |
| TnRadio | 单选 | `<TnRadio v-model="value" label="1">选项</TnRadio>` |
| TnSwitch | 开关 | `<TnSwitch v-model="checked" />` |
| TnSlider | 滑动选择 | `<TnSlider v-model="value" />` |
| TnNumberBox | 数字输入 | `<TnNumberBox v-model="count" />` |
| TnRate | 评分 | `<TnRate v-model="score" />` |
| TnSearchBox | 搜索 | `<TnSearchBox v-model="keyword" />` |

#### 🎯 选择器
| 组件 | 使用场景 | 快速示例 |
|------|----------|----------|
| TnPicker | 普通选择 | `<TnPicker v-model="value" :data="options" />` |
| TnDateTimePicker | 日期时间 | `<TnDateTimePicker v-model="date" mode="date" />` |
| TnRegionPicker | 地区选择 | `<TnRegionPicker v-model="region" />` |
| TnCalendar | 日历选择 | `<TnCalendar v-model="date" />` |

#### 💬 反馈提示
| 组件 | 使用场景 | 快速示例 |
|------|----------|----------|
| TnModal | 确认对话框 | `modalRef.value?.showModal({content: '提示'})` |
| TnNotify | 顶部通知 | `notifyRef.value?.show({msg: '成功'})` |
| TnActionSheet | 底部菜单 | `actionSheetRef.value?.show({actions: []})` |
| TnPopup | 自定义弹窗 | `<TnPopup v-model="show">内容</TnPopup>` |
| TnOverlay | 遮罩层 | `<TnOverlay v-model:show="show" />` |

#### 🎨 展示组件
| 组件 | 使用场景 | 快速示例 |
|------|----------|----------|
| TnSwiper | 轮播图 | `<TnSwiper :data="images" />` |
| TnProgress | 进度条 | `<TnLineProgress :percent="50" />` |
| TnLoading | 加载中 | `<TnLoading show animation />` |
| TnEmpty | 空状态 | `<TnEmpty mode="data" />` |
| TnBadge | 角标 | `<TnBadge value="99" />` |
| TnTag | 标签 | `<TnTag type="primary">标签</TnTag>` |
| TnAvatar | 头像 | `<TnAvatar url="..." />` |

#### 🧭 导航组件
| 组件 | 使用场景 | 快速示例 |
|------|----------|----------|
| TnNavbar | 顶部导航 | `<TnNavbar fixed>标题</TnNavbar>` |
| TnTabbar | 底部导航 | `<TnTabbar v-model="current">...</TnTabbar>` |
| TnTabs | 标签页 | `<TnTabs v-model="index">...</TnTabs>` |

---

## 常用代码片段

### 1. 完整表单示例
```vue
<script setup lang="ts">
import { reactive, ref } from 'vue'

const formRef = ref()
const formData = reactive({
  username: '',
  password: '',
  gender: '',
  agree: false
})

const rules = {
  username: [
    { required: true, message: '请输入用户名', trigger: 'blur' },
    { min: 3, max: 16, message: '长度3-16个字符', trigger: 'blur' }
  ],
  password: [
    { required: true, message: '请输入密码', trigger: 'blur' },
    { min: 6, message: '密码至少6位', trigger: 'blur' }
  ],
  gender: [
    { required: true, message: '请选择性别', trigger: 'change' }
  ]
}

const submit = () => {
  formRef.value?.validate((valid) => {
    if (valid) {
      // 提交表单
      console.log('表单数据:', formData)
    }
  })
}
</script>

<template>
  <TnForm ref="formRef" :model="formData" :rules="rules">
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
    
    <TnFormItem>
      <TnCheckbox v-model="formData.agree">同意用户协议</TnCheckbox>
    </TnFormItem>
  </TnForm>
  
  <view class="tn-p tn-mt">
    <TnButton type="primary" width="100%" @click="submit">提交</TnButton>
  </view>
</template>
```

### 2. 底部弹出选择器
```vue
<script setup lang="ts">
import { ref } from 'vue'

const showPicker = ref(false)
const pickerValue = ref('')
const pickerData = ['选项1', '选项2', '选项3']

const openPicker = () => {
  showPicker.value = true
}

const handleConfirm = (value) => {
  console.log('选中值:', value)
}
</script>

<template>
  <TnInput 
    v-model="pickerValue" 
    type="select" 
    placeholder="请选择"
    @click="openPicker"
  />
  
  <TnPicker
    v-model="pickerValue"
    v-model:open="showPicker"
    :data="pickerData"
    @confirm="handleConfirm"
  />
</template>
```

### 3. 图片上传功能
```vue
<script setup lang="ts">
import { ref } from 'vue'

const imageList = ref<string[]>([])
const actionUrl = 'https://your-api.com/upload/image'

const uploadSuccess = (file) => {
  console.log('上传成功:', file)
}

const uploadFail = (error, file) => {
  console.error('上传失败:', error)
}
</script>

<template>
  <TnImageUpload
    v-model="imageList"
    :action="actionUrl"
    :limit="9"
    @success="uploadSuccess"
    @fail="uploadFail"
  />
</template>
```

### 4. 轮播图展示
```vue
<script setup lang="ts">
import { ref } from 'vue'

const currentIndex = ref(0)
const bannerList = [
  'https://example.com/banner1.jpg',
  'https://example.com/banner2.jpg',
  'https://example.com/banner3.jpg',
]

const handleItemClick = (index) => {
  console.log('点击了第', index + 1, '个')
}
</script>

<template>
  <TnSwiper
    v-model="currentIndex"
    :data="bannerList"
    width="100%"
    height="420rpx"
    autoplay
    loop
    indicator
    indicator-type="dot"
    @item-click="handleItemClick"
  >
    <template #default="{ data }">
      <image class="swiper-image" :src="data" mode="aspectFill" />
    </template>
  </TnSwiper>
</template>

<style lang="scss" scoped>
.swiper-image {
  width: 100%;
  height: 100%;
  border-radius: 20rpx;
}
</style>
```

### 5. 列表加载更多
```vue
<script setup lang="ts">
import { ref } from 'vue'

const listData = ref([])
const loadmoreStatus = ref('loadmore')

const loadMore = async () => {
  if (loadmoreStatus.value !== 'loadmore') return
  
  loadmoreStatus.value = 'loading'
  
  try {
    // 模拟加载数据
    const newData = await fetchData()
    listData.value.push(...newData)
    
    if (newData.length === 0) {
      loadmoreStatus.value = 'nomore'
    } else {
      loadmoreStatus.value = 'loadmore'
    }
  } catch (error) {
    loadmoreStatus.value = 'loadmore'
  }
}
</script>

<template>
  <scroll-view scroll-y @scrolltolower="loadMore">
    <view v-for="item in listData" :key="item.id">
      {{ item.name }}
    </view>
    
    <TnLoadmore :status="loadmoreStatus" @click="loadMore" />
  </scroll-view>
</template>
```

### 6. 瀑布流布局
```vue
<script setup lang="ts">
import { ref } from 'vue'

const waterfallData = ref([
  { id: 1, url: 'https://...', height: 200 },
  { id: 2, url: 'https://...', height: 300 },
  // ...
])
</script>

<template>
  <TnWaterFall :data="waterfallData" mode="calc">
    <template #left="{ item }">
      <view class="waterfall-item">
        <image :src="item.url" mode="widthFix" />
      </view>
    </template>
    
    <template #right="{ item }">
      <view class="waterfall-item">
        <image :src="item.url" mode="widthFix" />
      </view>
    </template>
  </TnWaterFall>
</template>

<style lang="scss" scoped>
.waterfall-item {
  width: calc(100% - 20rpx);
  margin: 10rpx;
  border-radius: 15rpx;
  overflow: hidden;
  
  image {
    width: 100%;
    height: auto;
  }
}
</style>
```

### 7. 底部导航栏
```vue
<script setup lang="ts">
import { ref } from 'vue'

const currentTabbar = ref(0)

const tabbarData = [
  { name: '首页', icon: 'home', activeIcon: 'home-fill' },
  { name: '分类', icon: 'apps', activeIcon: 'apps-fill' },
  { name: '购物车', icon: 'shop', activeIcon: 'shop-fill', badge: '5' },
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
      :badge="item.badge"
    />
  </TnTabbar>
</template>
```

### 8. 自定义顶部导航
```vue
<script setup lang="ts">
const beforeBack = () => {
  // 返回前确认
  return new Promise((resolve) => {
    uni.showModal({
      title: '提示',
      content: '确定要返回吗？',
      success: (res) => {
        resolve(res.confirm)
      }
    })
  })
}
</script>

<template>
  <TnNavbar 
    fixed 
    bg-color="gradient__cool-5"
    text-color="#fff"
    :before-back="beforeBack"
  >
    <view class="tn-flex tn-align-center">
      <TnIcon name="logo-tuniao" class="tn-mr-sm" />
      <view>图鸟UI</view>
    </view>
    
    <template #right>
      <TnIcon name="setting" />
    </template>
  </TnNavbar>
</template>
```

---

## 常用样式组合

### 1. 卡片样式
```vue
<view class="tn-white_bg tn-radius tn-shadow tn-p">
  卡片内容
</view>
```

### 2. 完全居中
```vue
<view class="tn-flex-center">
  居中内容
</view>
```

### 3. 列表项
```vue
<view class="tn-white_bg tn-p tn-border-bottom">
  <view class="tn-flex tn-align-center">
    <TnIcon name="user" class="tn-mr" />
    <view class="tn-flex-1">用户名</view>
    <TnIcon name="right" color="tn-gray" />
  </view>
</view>
```

### 4. 标签组
```vue
<view class="tn-flex">
  <TnTag class="tn-mr-sm">标签1</TnTag>
  <TnTag class="tn-mr-sm">标签2</TnTag>
  <TnTag>标签3</TnTag>
</view>
```

### 5. 按钮组
```vue
<view class="tn-flex tn-flex-center">
  <TnButton class="tn-mr">取消</TnButton>
  <TnButton type="primary">确定</TnButton>
</view>
```

---

## TypeScript 类型支持

### 组件实例类型
```typescript
import type {
  TnButtonInstance,
  TnModalInstance,
  TnNotifyInstance,
  TnFormInstance,
  TnPickerInstance,
} from '@tuniao/tnui-vue3-uniapp'

const modalRef = ref<TnModalInstance>()
const formRef = ref<TnFormInstance>()
```

### 组件Props类型
```typescript
import type {
  FormRules,
  SwipeActionItemOption,
  BubbleBoxOption,
  LoadmoreStatus,
} from '@tuniao/tnui-vue3-uniapp'

const rules: FormRules = {
  username: [
    { required: true, message: '必填项' }
  ]
}
```

### 组件配置类型
```typescript
import type {
  AvatarIconProps,
  AvatarBadgeProps,
  TabsItemBadgeConfig,
} from '@tuniao/tnui-vue3-uniapp'
```

---

## 最佳实践速查

### ✅ 推荐做法

1. **使用内置样式类**
```vue
<!-- 好 -->
<view class="tn-p tn-white_bg tn-radius">内容</view>

<!-- 不推荐 -->
<view style="padding: 30rpx; background: #fff; border-radius: 15rpx;">内容</view>
```

2. **使用v-model双向绑定**
```vue
<!-- 好 -->
<TnInput v-model="username" />

<!-- 不推荐 -->
<TnInput :model-value="username" @update:model-value="username = $event" />
```

3. **使用ref调用组件方法**
```vue
<script setup>
const modalRef = ref()
const showModal = () => {
  modalRef.value?.showModal({ content: '提示' })
}
</script>

<template>
  <TnModal ref="modalRef" />
</template>
```

4. **表单验证**
```vue
<script setup>
const formRef = ref()

const submit = () => {
  formRef.value?.validate((valid) => {
    if (valid) {
      // 验证通过
    }
  })
}
</script>
```

5. **组件组合**
```vue
<!-- 好：语义清晰 -->
<TnForm>
  <TnFormItem label="用户名">
    <TnInput v-model="username" />
  </TnFormItem>
</TnForm>

<!-- 不好：缺少语义 -->
<view>
  <view>用户名</view>
  <TnInput v-model="username" />
</view>
```

---

## 常见问题快速解决

### Q1: 组件样式不生效？
```vue
<!-- 微信小程序中使用 -->
<TnButton custom-class="my-btn" :custom-style="{ fontSize: '32rpx' }">
  按钮
</TnButton>
```

### Q2: 如何阻止点击事件冒泡？
```vue
<TnButton click-modifiers="stop">按钮</TnButton>
```

### Q3: 表单验证不触发？
```vue
<!-- 确保设置了prop属性 -->
<TnFormItem label="用户名" prop="username">
  <TnInput v-model="formData.username" />
</TnFormItem>
```

### Q4: 弹窗如何拦截关闭？
```vue
<script setup>
const modalRef = ref()

modalRef.value?.showModal({
  content: '确定要退出吗？',
  confirm: () => {
    // 返回false阻止关闭
    return false
    
    // 或返回Promise
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve(true) // 允许关闭
        // reject() // 阻止关闭
      }, 1000)
    })
  }
})
</script>
```

### Q5: 如何实现自定义头部导航？
```vue
<template>
  <!-- 页面配置 -->
  <!-- pages.json中设置 "navigationStyle": "custom" -->
  
  <TnNavbar fixed>
    <view class="tn-flex tn-align-center">
      <TnIcon name="logo-tuniao" class="tn-mr-sm" />
      <view>标题</view>
    </view>
    
    <template #right>
      <TnIcon name="search" />
    </template>
  </TnNavbar>
  
  <!-- 页面内容 -->
  <view class="page-content">
    内容区域
  </view>
</template>
```

### Q6: 图片懒加载如何使用？
```vue
<template>
  <scroll-view scroll-y>
    <view v-for="item in imageList" :key="item.id" class="image-item">
      <TnLazyLoad 
        :src="item.url" 
        width="100%" 
        mode="widthFix"
        :threshold="100"
      />
    </view>
  </scroll-view>
</template>
```

---

## 组件搭配建议

### 1. 表单 + 验证
```
TnForm + TnFormItem + TnInput/TnCheckbox/TnRadio
```

### 2. 弹窗 + 内容
```
TnPopup + 自定义内容
TnModal（通过ref调用）
```

### 3. 导航 + 页面
```
TnNavbar（顶部） + 页面内容 + TnTabbar（底部）
```

### 4. 列表 + 加载
```
scroll-view + TnListItem循环 + TnLoadmore
```

### 5. 选择 + 展示
```
TnInput(type="select") + TnPicker
```

---

## 主题色对照表

| 类型 | 中文名 | 颜色值建议 | 使用场景 |
|------|--------|-----------|----------|
| primary | 主题色 | #01beff | 主要按钮、重要信息 |
| success | 成功色 | #09bb07 | 成功提示、完成状态 |
| warning | 警告色 | #ff976a | 警告提示、注意事项 |
| danger | 危险色 | #f56c6c | 删除操作、错误提示 |
| info | 信息色 | #909399 | 一般信息、辅助说明 |

---

## 组件尺寸对照表

| 尺寸 | 按钮高度 | 图标大小 | 字体大小 | 使用场景 |
|------|----------|----------|----------|----------|
| sm | 约60rpx | 约28rpx | 约24rpx | 紧凑布局、辅助按钮 |
| 默认 | 约80rpx | 约36rpx | 约28rpx | 常规使用 |
| lg | 约100rpx | 约44rpx | 约32rpx | 重要操作 |
| xl | 约120rpx | 约52rpx | 约36rpx | 特别强调 |

---

## 开发工具推荐

### VSCode插件
- **uni-helper** - uni-app代码提示
- **Vue Language Features (Volar)** - Vue3语法支持
- **TypeScript Vue Plugin (Volar)** - TS类型检查

### 开发配置
```json
// tsconfig.json
{
  "compilerOptions": {
    "types": ["@dcloudio/types"],
  }
}
```

---

## 性能优化建议

### 1. 按需加载组件
```typescript
// 只导入需要的组件
import TnButton from '@tuniao/tnui-vue3-uniapp/components/button/src/button.vue'
import TnInput from '@tuniao/tnui-vue3-uniapp/components/input/src/input.vue'
```

### 2. 图片优化
```vue
<!-- 使用懒加载 -->
<TnLazyLoad :src="imageUrl" />

<!-- 图片压缩 -->
<image :src="imageUrl" mode="aspectFill" lazy-load />
```

### 3. 列表优化
```vue
<!-- 使用虚拟列表 -->
<scroll-view scroll-y enhanced :show-scrollbar="false">
  <view v-for="item in visibleList" :key="item.id">
    {{ item.name }}
  </view>
</scroll-view>
```

### 4. 避免频繁更新
```vue
<script setup>
import { ref, computed } from 'vue'

// 使用computed缓存计算结果
const formattedData = computed(() => {
  return data.value.map(item => ({
    ...item,
    label: formatLabel(item)
  }))
})
</script>
```

---

## 调试技巧

### 1. 查看组件实例
```vue
<script setup>
const buttonRef = ref()

onMounted(() => {
  console.log('按钮实例:', buttonRef.value)
})
</script>

<template>
  <TnButton ref="buttonRef">按钮</TnButton>
</template>
```

### 2. 监听组件事件
```vue
<TnTabs 
  v-model="currentTab"
  @change="(val) => console.log('标签改变:', val)"
>
  <TnTabsItem title="标签1" />
  <TnTabsItem title="标签2" />
</TnTabs>
```

### 3. 使用开发工具
```vue
<!-- 添加边框查看布局 -->
<view style="border: 1px solid red;">
  调试内容
</view>

<!-- 添加背景色查看层级 -->
<view style="background: rgba(255, 0, 0, 0.1);">
  调试内容
</view>
```

---

## 更新日志参考

根据官方文档，图鸟UI保持持续更新，主要包括：
- 修复已知bug
- 新增组件功能
- 性能优化
- 平台适配改进

建议定期查看官方文档了解最新变更：https://vue3.tuniaokj.com/doc/guide/changelog.html

---

## 相关链接

- 官方网站：https://vue3.tuniaokj.com
- GitHub仓库：https://github.com/tuniaoTech/tuniaoui-vue3-uniapp
- npm包：https://www.npmjs.com/package/@tuniao/tnui-vue3-uniapp
- 图鸟图标：https://www.npmjs.com/package/@tuniao/tn-icon

---

## 总结

本快速参考手册涵盖了：
- ✅ 快速安装和引入方式
- ✅ 按使用场景分类的组件列表
- ✅ 常用代码片段和完整示例
- ✅ 最佳实践和开发建议
- ✅ 常见问题快速解决方案
- ✅ TypeScript类型支持
- ✅ 性能优化技巧
- ✅ 调试方法

建议收藏本文档，在开发过程中快速查阅！

