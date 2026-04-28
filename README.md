# Basic Design Check

一句话描述：
上传 UX 设计作品，从排版、配色、规范性等维度进行批阅，在原图上标注问题和亮点，给出改进建议。

One-line description:
Upload a UX design work, review it on typography, color, and design standards, annotate issues and strengths on the original image, and provide actionable improvement suggestions.

---

basic-design-check 是一个面向 UX 新人的设计作品批阅技能。

它会对上传的设计稿进行专业维度的检查，核心能力包括：

- 排版检查（对齐、间距、字号层级、行高、留白、网格感）
- 配色检查（对比度、和谐性、可读性、情绪匹配）
- 规范性检查（组件一致性、圆角统一、边距规律、设计系统遵循度）

basic-design-check is a skill for reviewing UX design works aimed at beginners.
It performs professional-level checks on uploaded designs with:

- Typography review (alignment, spacing, font hierarchy, line height, whitespace, grid)
- Color review (contrast, harmony, readability, mood matching)
- Standards review (component consistency, border radius, margins, design system adherence)

## 当前版本 / Current Version

当前为第一版：多维度批阅版。

针对不同类型的设计稿（排版练习、配色练习、规范化练习、综合页面、单个组件）自动调整检查重点和标注密度。

Current version: V1, multi-dimension review.

Automatically adapts review focus and annotation density based on design type (typography exercise, color exercise, standardization exercise, full page, single component).

## 通用安装（IDE / Agent） / Universal Install (IDE / Agent)

```bash
git clone https://github.com/YOUR_USERNAME/basic-design-check.git
```

然后在你的 IDE / Agent 工具里，把 basic-design-check 目录作为技能目录或本地能力目录加载。

Then load the basic-design-check folder in your IDE/agent as a local skill/capability directory.

常见用法 / Common patterns:

- **Cursor**: add this repo as a local prompt/skill source
- **Claude Code**: reference this repo folder as a reusable skill prompt pack
- **Codex**: install from GitHub URL or copy folder into your skills directory
- **Mira**: 打包为 zip 上传安装

## 如何触发 / How to Trigger

你可以用以下方式触发 / Trigger in these ways:

1. 技能名调用：`basic-design-check`
2. 自然语言："帮我看看这个设计稿" / "检查一下我的作业" / "review my design"

## 默认行为 / Default Behavior

中文：

- 用户上传图片后，默认先直接生成批阅标注图，再补充文字改进建议
- 多张图片默认逐张独立批阅，不合并
- 默认使用"基于上传图片编辑"的能力，在原图上只叠加标注层
- 必须保留原图所有设计元素、比例、背景色不变
- 红色标记问题区域，绿色标记亮点区域
- 当标注色与背景色冲突时，自动加白色描边确保可读
- 每条标注指向具体位置，问题附带改进方向，亮点说明好在哪里

English:

- When image input is present, generate the annotated review image first, then explain
- Multiple uploaded images are processed independently by default
- Use image editing to overlay annotation layer on the original design
- Preserve all design elements, proportions, and background colors
- Red marks for issues, green marks for strengths
- White outlines added when annotation colors conflict with background
- Every annotation points to a specific location with actionable feedback

## 仓库结构 / Repository Structure

```
basic-design-check/
├── SKILL.md          # 技能定义文件
├── README.md         # 说明文档
```

## 更新技能 / Update the Skill

如果用 git clone 安装：

```bash
git pull origin main
```

## 备注 / Notes

- 如果你希望别人直接安装，仓库建议设为 public
- 如果仓库是 private，别人需要访问权限或 token 才能安装
