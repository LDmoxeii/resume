# CLAUDE_CN.md

此文件为 Claude Code (claude.ai/code) 在此代码库中工作时提供指导。

## 项目概述

这是一个基于冰岩工作室 LapisCV 项目的**简历创建工具包**。它是一个配置好的 Obsidian 知识库，用于使用 Markdown 和自定义 CSS 样式以及嵌入字体创建专业简历。

**这不是传统的软件项目** - 它没有构建脚本、package.json 或测试套件。相反，它是一个为简历/CV 生成优化的文档创建系统。

## 关键组件

### 简历文件
- `template-cn.md` / `template-en.md`: 中英文简历基础模板
- `resume-cn.md`: 当前工作简历文件

### 样式系统
- `.obsidian/snippets/lapis-cv.css`: 主题样式，嵌入中文字体 (思源黑体、JetBrainsMono)
- `.obsidian/snippets/lapis-cv-serif.css`: 衬线字体变体主题
- 两个 CSS 文件都约 45MB，因为嵌入了字体以实现自包含操作

### 配置
- `.obsidian/app.json`: PDF 导出设置 (A4，1mm 边距，98% 缩放)
- `.obsidian/appearance.json`: 主题配置 (Moonstone 主题，强调色 #4870ac)

## 常用操作

### 编辑简历
- 直接编辑 markdown 文件 (`template-cn.md`, `resume-cn.md` 等)
- 使用标准 markdown 语法和 HTML 元素进行样式设置
- 图标使用自定义字体: `<span class="icon">&#xe60f;</span>` 表示电话，`<span class="icon">&#xe7ca;</span>` 表示邮箱
- 章节标题: `## <span>&#xe80c;</span> 教育经历`

### 样式自定义
- 修改 `.obsidian/snippets/lapis-cv.css` 中的 CSS 变量:
  - `--accent-color`: 主题色 (#4870ad)
  - `--avatar-width`: 头像大小
  - `--text-color`: 主文本颜色 (#353a42)
- 将头像改为方形而不是圆形: 将 `border-radius: 50%` 改为 `border-radius: 0`
- 始终注释掉旧的 CSS 规则而不是删除它们

### 内容结构
- 使用 `<div class="entry-title">` 作为项目/工作标题，带有日期
- 头像图片: `<img class="avatar" src="filename.jpg">`
- 联系信息使用带特定 Unicode 字符的图标 span
- 技术技能用嵌套列表组织，用 **粗体** 标记关键词

### PDF 导出
- 使用 Obsidian 内置的 PDF 导出 (Ctrl+P)
- 设置在 `.obsidian/app.json` 中预配置
- 导出为专业边距的 A4 打印优化

## 架构说明

### 字体系统
- 自包含，嵌入中文字体 (思源黑体、思源宋体)
- 自定义图标字体 (LapisCV Icon) 用于UI元素
- JetBrainsMono 用于代码/技术文本
- 无外部字体依赖

### 配色方案
- 主强调色: #4870ad (专业蓝色)
- 文本: #353a42 (深灰色，便于阅读)
- 边框: #dae3ea (淡灰色)
- 所有颜色定义为 CSS 变量，便于自定义

### 布局系统
- 使用 CSS Grid 和 Flexbox 实现响应式设计
- 为 PDF 导出优化，不是网页显示
- 右对齐头像，浮动定位
- 条目标题使用 flex 布局实现标题/日期对齐

## 文件命名约定
- 模板: `template-{lang}.md`
- 工作文件: `resume-{lang}.md` 或描述性名称
- 图片: 放在根目录，直接通过文件名引用
- 备份文件: 使用描述性名称如 `oldCV.md`

## 当前用户背景
用户是一名 Java 后端开发实习生，经验包括:
- Spring 生态系统 (SpringBoot, MyBatis, Spring AOP)
- 数据库技术 (MySQL, Redis)
- 分布式系统和微服务
- 开源贡献 (cap4j 框架)

进行更改时，为软件工程职位保持专业格式和技术准确性。