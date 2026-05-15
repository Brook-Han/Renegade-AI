# Renegade AI v5.3 — 参考文献验证报告

**验证日期**: 2026-05-15  
**验证方法**: 三级验证——DOI 交叉引用解析、arXiv API 匹配、WebSearch 论文存在性验证  
**总参考文献数**: 29 条  
**验证通过**: 29/29（所有论文/书籍均真实存在）  
**有问题需修正**: 7 条

---

## 验证方法说明

每条参考文献按以下层级逐一验证：

| 层级 | 适用条件 | 方法 |
|------|---------|------|
| L1: DOI 解析 | 有 DOI | WebSearch 定位论文 → 交叉比对标题、作者、期刊、年份 |
| L2: arXiv 匹配 | 有 arXiv ID | WebSearch arXiv 页面 → 比对标题、作者、版本号 |
| L3: 论文搜索 | 无 DOI/arXiv | WebSearch 搜索论文标题 + 作者 → 确认存在并比对字段 |

对每条文献检查：论文真实性、标题匹配度、作者匹配度、期刊/出版方、年份、DOI 有效性。

---

## 一、完全正确的参考文献（22条）

| # | 参考文献 | 状态 |
|---|---------|------|
| 1 | Akbulut et al. (2026) — arXiv:2603.25326 | ✅ 存在，见下方注意事项 |
| 2 | Binz et al. (2025) — Nature | ✅ |
| 3 | Candrian & Scherer (2022) — Computers in Human Behavior | ✅ |
| 4 | Cheng et al. (2026) — Science | ✅ |
| 5 | Eloundou et al. (2023) — arXiv:2303.10130 | ✅ |
| 6 | Evans et al. (2026) — Science | ✅ |
| 7 | Floridi (2014) — OUP | ✅ |
| 8 | Falk & Tsoukalas (2026) — arXiv:2603.20617 | ✅ |
| 9 | Glickman & Sharot (2025) — Nature Human Behaviour | ✅ |
| 10 | Hao et al. (2026) — Nature | ✅ |
| 11 | Horowitz & Kahn (2024) — International Studies Quarterly | ✅ |
| 12 | Hoberg (2026) — Frontiers in Psychology | ✅ |
| 13 | Ibrahim et al. (2026) — Nature | ✅ |
| 14 | Jussupow et al. (2024) — MIS Quarterly | ✅ |
| 15 | Kusumegi et al. (2025) — Science | ✅ |
| 16 | Lenski et al. (1999) — Nature | ✅ |
| 17 | Moravec (1988) — Harvard UP | ✅ |
| 18 | Müller et al. (2026) — PNAS | ✅ |
| 19 | Oh et al. (2025) — Nature | ✅ |
| 20 | Ray (1992) — Addison-Wesley | ✅ |
| 21 | Salvi et al. (2025) — Nature Human Behaviour | ✅ |
| 22 | Shaw & Nave (2026) — Wharton | ✅ |

---

## 二、存在的问题（7条）

### 🔴 严重问题（建议立即修正）

#### 1. Vashistha et al. (2024) — 标题错误 + 发表渠道错误

**书稿中写的内容**:
> Vashistha, A., Naaman, M., et al. (2024). AI writing assistants shift users toward Western cultural norms. *Proceedings of the ACM on Human-Computer Interaction*, 8(CSCW2), Article 312.

**实际论文信息**:
- **标题**: "AI Suggestions Homogenize Writing Toward Western Styles and Diminish Cultural Nuances"
- **作者**: Dhruv Agarwal, Mor Naaman, Aditya Vashistha（注意：书稿中缺少第一作者 Agarwal）
- **发表渠道**: 被 CHI 2025 接收，**不是** PACMHCI CSCW
- **arXiv**: 2409.11360

**建议修正**:
> Agarwal, D., Naaman, M., & Vashistha, A. (2024). AI suggestions homogenize writing toward Western styles and diminish cultural nuances. *arXiv preprint arXiv:2409.11360*. (Accepted at CHI 2025).

---

#### 2. Chen et al. (2026) — 标题错误

**书稿中写的内容**:
> Chen, E. K., Belkin, M., Bergen, L., & Danks, D. (2026). Is artificial general intelligence here? *Nature*, Comment.

**实际的 Nature 文章标题**:
> "Does AI already have human-level intelligence? The evidence is clear"

**建议修正**:
> Chen, E. K., Belkin, M., Bergen, L., & Danks, D. (2026). Does AI already have human-level intelligence? The evidence is clear. *Nature*, 650, 36–40.

---

#### 3. Luettgau et al. (2025) — 标题错误

**书稿中写的内容**:
> Luettgau, L., et al. (2025). How readily do humans follow personal advice from large language models? *arXiv preprint arXiv:2511.15352v3*.

**实际的 arXiv 标题**:
> "People readily follow personal advice from AI but it does not improve their well-being"

**额外问题**: 最新版本为 v2，非 v3。

**建议修正**:
> Luettgau, L., Cheung, V., Dubois, M., et al. (2025). People readily follow personal advice from AI but it does not improve their well-being. *arXiv preprint arXiv:2511.15352*.

---

### 🟡 中等问题（建议核实后修正）

#### 4. Rainey & Hochberg (2025) — DOI 可能错误

**书稿中的 DOI**: `10.1073/pnas.2421525122`  
**搜索到的 DOI**: `10.1073/pnas.2509122122`

两篇都为 PNAS 论文，且作者、期刊、年份均匹配。书稿中的 DOI 可能是另一个 PNAS 条目或是早期版本编号。**建议向 PNAS 核实正确的 DOI**。

**建议修正**（待核实后）:
> Rainey, P. B., & Hochberg, M. E. (2025). Could humans and AI become a new evolutionary individual? *Proceedings of the National Academy of Sciences*, 122(37), e2509122122. https://doi.org/10.1073/pnas.2509122122

---

#### 5. Kosmyna et al. — 年份标注为 2024，实际为 2025

**书稿中写的内容**:
> Kosmyna, N., et al. (2024). Your brain on ChatGPT: Accumulation of cognitive debt when using AI assistant for essay writing tasks. *MIT Media Lab Working Paper*.

实际论文在 arXiv 上的发布日期为 2025年6月10日。描述为 "MIT Media Lab Working Paper" 可以接受，但年份应改为 2025。

**建议修正**:
> Kosmyna, N., et al. (2025). Your brain on ChatGPT: Accumulation of cognitive debt when using AI assistant for essay writing tasks. *MIT Media Lab Working Paper*.

---

### 🟢 轻微问题

#### 6. Akbulut et al. (2026) — arXiv 版本号错误

**书稿中写的内容**: `arXiv:2603.25326v4`  
**arXiv 上最新版本**: v3（2026年4月2日）

**建议修正**: `arXiv:2603.25326`

---

#### 7. Wenger et al. (2026) — DOI 链接格式问题

书稿中的 DOI 链接格式正确但末尾有多余的点号：`[https://doi.org/10.1038/s44271-025-00387-3](https://doi.org/10.1038/s44271-025-00387-3).` → 应移除末尾句号外的闭合括号。

---

## 三、验证统计

| 类别 | 数量 | 占比 |
|------|------|------|
| 完全正确 | 22 | 75.9% |
| 轻微问题 | 2 | 6.9% |
| 中等问题 | 2 | 6.9% |
| 严重问题 | 3 | 10.3% |
| **总计** | **29** | **100%** |

**关键发现**: 所有 29 条参考文献指向的论文/书籍都是真实存在的，未发现任何"幻觉"引用（即完全编造的论文）。但 4 条存在标题错误（其中 3 条差异显著），1 条 DOI 待核实，1 条年份错误，1 条版本号错误。

---

## 四、系统性建议

1. **每次新增引用时**，同步录入 DOI 或 arXiv ID，并在提交前至少用一次 WebSearch 核验标题是否与出版源一致。

2. **建立引用录入标准**：标题应从原始出处（DOI 页面 / arXiv 页面）直接复制，而非凭记忆或重新措辞。

3. **arXiv 论文的版本号**建议不加，或使用不加版本号的形式（`arXiv:XXXX.XXXXX`），因为版本号会随时间推移而过时。

4. **"et al." 的使用**：如果第一作者在书稿正文中的定性陈述中起关键作用（例如 Vashistha 的论文实际由 Agarwal 领导），建议在参考文献中列出更多作者姓名。
