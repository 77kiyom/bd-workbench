# 寄样工作台

一个集成式的寄样管理工作台页面，整合了常用的寄样信息处理功能。

**仓库地址**：https://github.com/77kiyom/bd-workbench

修改方法、部署到 GitHub Pages、常用改动位置速查，见 [GITHUB_SETUP.md](GITHUB_SETUP.md)。

## 功能特性

### 🎯 核心功能

1. **📋 寄样信息整理**
   - 从飞书表格读取寄样信息
   - 自动匹配 SKU 和解析地址
   - 生成整理后的数据并回写

2. **📦 批量录入生成**
   - 从整理表读取数据
   - 按单价计算总额
   - 拆分成多个 Excel 录入文件（单文件不超 1000 元）

3. **🚚 快递单号同步**
   - 从网易营销平台获取快递单号
   - 自动同步物流状态
   - 支持增量更新和飞书通知

4. **📖 查看使用说明**
   - 快速访问完整操作文档

### 🔗 快捷链接

- 飞书达人信息表
- 云端技能文档
- 使用说明文档
- 网易营销平台
- 本地录入文件输出目录

## 在线访问

- **编辑链接**：https://www.workbuddy.ai/space/d/3itRrQoWU5q1Tq8Im8vhc2
- **分享链接**：https://workbuddy.cc/p/3itRrQoWU5q1Tq8Im8vhc2

## 本地使用

直接在浏览器中打开 `workbench.html` 文件即可使用。

## 技术栈

- 纯 HTML + CSS + JavaScript
- 响应式设计
- 现代化 UI 设计（渐变背景 + 卡片式布局）

## 相关资源

- [寄样信息整理技能文档](https://www.workbuddy.ai/space/d/dDzi175uGsGbPKBHIw7Ozn)
- [使用说明文档](https://www.workbuddy.ai/space/d/l4DX9SzWstfjA311UIyOi3)
- [飞书达人信息表](https://kttfkmbfmy.feishu.cn/sheets/NlFwsEJu6h3QL1tR7SccvEq3nYd)

## 更新日志

### 2026-10-19
- 初始版本发布
- 集成四大核心功能卡片
- 添加快捷链接区域
