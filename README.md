# 🍃Floristic - 让大地穿上会呼吸的衣服
Floristic 是一个基于 SDF（Signed Distance Function）的、完全开放的植被生成平台，让任何人都能用 JSON 定义数学定义的树木，并与 Tectonic 的地形无缝共存。

![Static Badge](https://img.shields.io/badge/License-MIT-yellow.svg)
![Static Badge](https://img.shields.io/badge/Minecraft-1.20.1-success)
![Static Badge](https://img.shields.io/badge/Forge-47.1.0-orange)
## ✨ 核心特性
### 🌳 数学定义的树木
* **不再有预制结构**：每棵树都由 SDF 数学公式实时生成

* **无限变体**：通过调整参数，可以创造任何形态的树木

* **弯曲的树干**：用样条曲线实现自然弯曲

* **发光的树冠**：支持任意方块，包括模组方块

### 🎨 完全开放的设计
* **JSON 配置**：所有树木形态都通过 JSON 定义

* **KubeJS 集成**：可动态调整生成规则

* **Java API**：供模组开发者扩展新形状

* **数据包兼容**：完美融入原版数据包系统

### ⚡ 性能优先
* **LOD 框架**：根据玩家距离动态调整生成精度

* **智能缓存**：重复的树形配置只计算一次

* **渐进式生成**：巨型树木分批次放置，避免卡顿

### 🔗 生态兼容
* **与 Tectonic 完美共存**：在 Tectonic 的山脉上生成你的树

* **与原版群系兼容**：可在任何原版群系中使用

* **与其他模组协作**：通过 KubeJS 与其他模组联动
## 🏗️ 架构概览
Floristic Core
├── SDF 算法库
│   ├── 基础图元（球体、圆锥、圆柱、样条曲线）
│   ├── 布尔运算（并集、差集、交集、平滑并集）
│   └── 变换（平移、旋转、缩放、扭曲）
│
├── LOD 框架
│   ├── 感知层（监控玩家位置、TPS、区块状态）
│   ├── 决策层（动态决定生成精度）
│   └── 执行层（按 LOD 等级生成树木）
│
├── Feature 系统
│   ├── SDFTreeFeature（原版 Feature 实现）
│   ├── SDFTreeConfig（JSON 配置类）
│   └── TreeRegistry（注册自定义树木类型）
│
├── 缓存系统
│   ├── 树形缓存（重复配置免计算）
│   ├── 区块缓存（预生成结果）
│   └── LOD 缓存（不同精度版本）
│
└── API 层
    ├── Java API（供模组开发者扩展）
    ├── JSON Schema（供整合包作者配置）
    └── KubeJS 绑定（供脚本动态调整）
## 📦 快速开始
安装
下载 Floristic 模组，放入 mods 文件夹

* （⭐**建议**⭐）安装 Tectonic 获得最佳体验

* （⭐**可选**⭐）安装 KubeJS 获得动态配置能力
## 📚 文档
完整文档

SDF 形状参考

LOD 配置指南

KubeJS 集成

API 文档

## 🤝 贡献
Floristic 是一个开放平台，欢迎所有形式的贡献：

提交 Issue：报告 bug 或提出新功能

Pull Request：改进代码或文档

分享配置：把你创造的树木分享给社区

写教程：帮助更多人上手

## 📄 许可证
MIT License © 2024 [Elyuis]

## 🙏 致谢
Tectonic 团队，启发了开放平台的设计理念

BCLib 团队，SDF 算法的先驱

Minecraft Forge 社区，提供技术支持
