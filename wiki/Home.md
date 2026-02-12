# 中小学智慧营养膳食管理平台

## 项目简介

G-B-C（Government-Business-Consumer）一体化营养膳食监管与服务平台，面向教育局、学校和家长三端用户，提供从营养膳食规划、监管到服务的全链路数字化解决方案。

## 项目结构

```
school-nutrition-system/
├── index.html                    # 平台入口页面
├── shared/
│   └── css/
│       └── common.css            # 全局共享样式
├── education-bureau/             # 教育局端
│   ├── dashboard.html            # 数据驾驶舱
│   ├── dish-library.html         # 公共菜肴库管理
│   ├── recipe-template.html      # 公共周食谱模板
│   ├── warning-monitor.html      # 营养监测预警
│   └── dining-data.html          # 学生就餐数据监管
├── school/                       # 学校端
│   ├── recipe-editor.html        # 周食谱智能编排
│   ├── dish-library.html         # 校本菜肴库
│   ├── nutrition-analysis.html   # 营养分析报表
│   ├── student-profile.html      # 学生营养档案
│   └── dashboard.html            # 校级数据看板
├── parent/                       # 家长端（移动端）
│   ├── index.html                # 首页
│   ├── order.html                # 在线点餐
│   ├── satisfaction.html         # 满意度评价
│   ├── nutrition-report.html     # 营养摄入报告
│   ├── traceability.html         # 食材溯源
│   └── weekly-recipe.html        # 完整周食谱
└── wiki/                         # 项目文档
```

## 快速开始

1. 克隆仓库
2. 在项目根目录启动任意 HTTP 服务器：
   ```bash
   python -m http.server 8080
   ```
3. 浏览器访问 `http://localhost:8080`

## 技术栈

- 纯 HTML5 + CSS3，无框架依赖
- CSS 自定义属性（变量）实现主题系统
- 响应式布局（桌面端 + 移动端适配）
- CSS 可视化图表（柱状图、环形图、进度条）
