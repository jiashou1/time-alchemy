# 时间炼金术 (Time Alchemy)

> 一款时间追踪与 AI 复盘的单页应用

## 项目概述

- **版本**: v1.7.5
- **技术栈**: React 18 + Tailwind CSS + Babel (CDN 引入)
- **入口文件**: `index.html`

## 核心功能

### 1. 时间记录

- **计时器** - 开始/停止记录时间，实时显示已过时长
- **分类系统** - 6 大预设分类
  | 分类 | ID | 颜色 |
  |------|-----|------|
  | 交易研究 | CORE | 绿色 #00ff41 |
  | AI探索 | AI | 蓝色 #0ea5e9 |
  | 家庭时光 | FAMILY | 粉色 #ec4899 |
  | 休闲娱乐 | RECREATION | 紫色 #8b5cf6 |
  | 无效损耗 | WASTE | 红色 #ef4444 |
  | 日常代谢 | RECHARGE | 黄色 #eab308 |
- **快捷标签** - 每个分类下可配置子标签，快速标记活动类型
- **备注** - 活动期间可记录感想
- **补录** - 支持补填历史时间段

### 2. 即时想法 (IDEA)

快速记录瞬时灵感，独立卡片展示

### 3. 记录管理

- 按时间倒序展示所有记录
- 编辑/删除历史记录
- 自动同步到云端

### 4. AI 智能复盘

- **数据可视化** - 环形图展示时间分布
- **Gemini AI 分析** - 调用 Gemini API 分析时间使用情况
- **对话追问** - 可继续与 AI 讨论，获得改进建议
- **支持今日/本周复盘**

### 5. 数据同步与导出

- GitHub Gist 云端备份与跨设备同步
- 一键导出全部记录到剪贴板

## 数据存储

本地数据存储在 `localStorage`:

| Key | 说明 |
|-----|------|
| `timeLogs` | 时间记录数组 |
| `activeTask` | 当前进行中的任务 |
| `syncConfig` | 同步配置 |
| `activeFeeling` | 当前任务备注 |
| `activeCategory` | 当前任务分类 |
| `activeQuickTags` | 当前任务选中的标签 |

## 配置项 (syncConfig)

```json
{
  "token": "GitHub Token",
  "gistId": "Gist ID for sync",
  "tagMap": "分类标签配置",
  "apiKey": "Gemini API Key",
  "modelName": "gemini-3-flash-preview"
}
```

## 默认标签配置

```
交易研究:复盘,盯盘,开仓;
AI探索:提示词,测试,阅读;
家庭时光:配偶,孩子,父母;
日常代谢:睡觉,饮食,洗漱,如厕
```

## 设计风格

- 暗色主题，绿色终端风格 (#0a0a0a 背景, #00ff41 主色)
- JetBrains Mono 等宽字体
- Glass morphism 卡片效果
- 移动端优先的响应式设计

## 使用方法

直接用浏览器打开 `index.html` 即可使用。

## 依赖 (CDN)

- React 18
- ReactDOM 18
- Babel (standalone)
- Tailwind CSS
