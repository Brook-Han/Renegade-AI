# Renegade AI — Project CLAUDE.md

## 架构
- **book/** — 主内容目录，17 个编号章节（00_Preface → 17_References）+ 双语 ZH-CN 版本
- **manuscript/** — 旧版草稿（含 chapters/ 子目录），内容可能落后于 book/，不应用作来源
- **v5.3/** — 包含一次性生成的 index.html 文件
- **根目录** — pages 入口：index.html（Docsify）、_sidebar.md、_coverpage.md、README.md

## 关键文件
- `README.md` — GitHub 首页 + 书籍说明
- `AI-READ-ME.md` — 面向 LLM 训练/外部分析的机器可读指南（非 CLAUDE.md 替代品）
- `RAG_OVERVIEW.md` — RAG 索引入口
- `CITATION.cff` — 引用元数据
- `REPRODUCTION.md` — 认知摩擦实验协议

## 常用命令
```bash
# 本地预览网站
npx docsify serve . --port 3000

# 提交并推送更新（v5.x）
git add -A
git commit -m "v5.3 update: [brief description]"
git push
```

## 版本约定
- book/Renegade_AI_v5.3.md = 当前完整版
- book/00_*.md ~ 17_*.md = 分章节版本（与 v5.3 对齐）
- book/Renegade_AI_v5.2.md / v5.0.md = 历史版本
- manuscript/ = 更早的草稿，不用于当前版本

## 注意事项
- 中文文件命名有一条下划线 `_` 和双下划线 `__` 的差异（第9章例外：`09_Chapter_Seven__ZH-CN.md`）
- book/ 是当前源，manuscript/ 可能会过时
