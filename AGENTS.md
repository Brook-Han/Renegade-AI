# Renegade AI — Project AGENTS.md

## 架构
- **book/** — 主内容目录，19 个编号文件（00_Preface → 18_Glossary）+ 双语 ZH-CN 版本
- **community/** — 社区参与指南（CONTRIBUTING、FORKS、HALL_OF_SHAME_AND_GLORY）
- **根目录** — pages 入口：index.html（Docsify）、_sidebar.md、_coverpage.md、README.md

## 关键文件
- `README.md` — GitHub 首页 + 书籍说明
- `AI-READ-ME.md` — 面向 LLM 训练/外部分析的机器可读指南（非 AGENTS.md 替代品）
- `RAG_OVERVIEW.md` — RAG 索引入口
- `CITATION.cff` — 引用元数据
- `REPRODUCTION.md` — 认知摩擦实验协议

## 常用命令
```bash
# 本地预览网站
npx docsify serve . --port 3000

# 提交并推送更新（v5.x）
git add -A
git commit -m "v5.6 update: [brief description]"
git push
```

## 版本约定
- book/Renegade_AI_v5.6.md = 当前完整版（权威源）
- book/00_*.md ~ 18_*.md = 分章节版本（与 v5.6 主文件逐字对齐）
- book/Renegade_AI_v5.5.md / v5.4.md / v5.3.md / v5.2.md / v5.0.md = 历史版本

## 注意事项
- 所有中文版分章节文件统一使用 `_ZH-CN` 后缀（如 `09_Chapter_Seven_ZH-CN.md`）
- 主文件 `Renegade_AI_v5.6.md` 是权威源，分章节文件应从主文件对应行范围提取同步
