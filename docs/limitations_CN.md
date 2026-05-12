# 已知限制

[← 返回 README](../README_CN.md)

- **原生 UML 标记**:tldraw 箭头有限(不支持继承所需的空心三角形)。学术论文中的严格 UML/ERD 图请使用 drawio-skill
- **无原生容器/泳道**:tldraw 的分组模型与 drawio 不同。请用颜色和间距实现视觉分组
- **不支持 PDF 导出**:tldraw-cli 仅支持 PNG 和 SVG。如需 PDF,可将 SVG 后处理转换(如 `rsvg-convert`)
- **自检需要视觉能力**:自动修复步骤通过模型的视觉能力读取 PNG。不支持视觉的模型会跳过此步
