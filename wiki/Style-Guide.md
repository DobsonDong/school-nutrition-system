# 样式系统说明

## 全局样式文件

`shared/css/common.css` 是项目唯一的全局样式文件，基于 CSS 自定义属性构建主题系统。

## CSS 变量

```css
--primary: #667eea       /* 主色调 */
--primary-dark: #5a67d8  /* 主色深色 */
--success: #10b981       /* 成功/达标 */
--warning: #f59e0b       /* 警告 */
--danger: #ef4444        /* 危险/紧急 */
--accent: #f59e0b        /* 强调色 */
--gray-50 ~ --gray-900   /* 灰度色阶 */
```

## 布局系统

| 类名 | 说明 |
|------|------|
| `.layout` | 左右布局容器（侧边栏 + 主内容） |
| `.sidebar` | 左侧导航侧边栏（240px） |
| `.main-content` | 右侧主内容区 |
| `.page-content` | 页面内容内边距区域 |
| `.grid.grid-2~5` | 2-5列栅格布局 |

## 通用组件

### 卡片 `.card`
```html
<div class="card">
    <div class="card-header">
        <div class="card-title">标题</div>
    </div>
    <div class="card-body">内容</div>
    <div class="card-footer">底部</div>
</div>
```

### 统计卡片 `.stat-card`
```html
<div class="stat-card">
    <div class="stat-icon blue">📊</div>
    <div class="stat-content">
        <div class="stat-label">标签</div>
        <div class="stat-value">数值</div>
        <div class="stat-change up"><span>↑</span><span>变化</span></div>
    </div>
</div>
```

### 按钮 `.btn`
- `.btn-primary` 主要按钮
- `.btn-secondary` 次要按钮
- `.btn-ghost` 幽灵按钮
- `.btn-danger` 危险按钮
- `.btn-sm` 小尺寸

### 标签 `.tag`
- `.tag-blue` / `.tag-green` / `.tag-orange` / `.tag-red`

### 表格 `.data-table`
- `.table-container` 表格滚动容器
- `.data-table` 数据表格

### 分页 `.pagination`
- `.page-btn` 分页按钮
- `.page-btn.active` 当前页

### 表单
- `.form-input` 输入框
- `.form-select` 下拉选择
- `.search-box` 搜索框组件

### 导航
- `.nav-item` 侧边栏导航项
- `.nav-item.active` 当前激活项
- `.nav-item-badge` 徽标数字

## 移动端样式

家长端页面使用独立的内联样式，采用 `max-width: 480px` 容器布局，包含：
- `.mobile-container` 移动端容器
- `.mobile-header` 顶部固定头
- `.bottom-nav` 底部导航栏

## CSS 可视化图表

项目使用纯 CSS 实现数据可视化，无需 JavaScript 图表库：

- **柱状图**：`flex` + `height` 百分比 + `linear-gradient` 背景
- **环形图**：`conic-gradient` 背景 + 圆形遮罩
- **进度条**：嵌套 `div` + `width` 百分比 + 渐变背景
- **对比条**：`position: absolute` 实现标准线标注
