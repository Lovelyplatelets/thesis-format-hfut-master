---
name: thesis-format-hfut-master
description: Convert a thesis Markdown file with YAML frontmatter into a Word .docx formatted for Hefei University of Technology master's degree dissertations. Use when the user asks to format, typeset, generate, or repair an HFUT master's thesis/dissertation Word document, especially for 学历硕士/专业硕士论文, 合肥工业大学研究生学位论文写作规范, thesis front matter, abstracts, TOC, figures/tables, references, appendices, and academic achievements lists.
---

# 合肥工业大学硕士学位论文格式化

## 功能

将带 YAML frontmatter 的 Markdown 论文转换为符合《合肥工业大学研究生学位论文写作规范》和学历硕士示例的 `.docx`。该技能参考 `wojintiantouhentong/thesis-format-hfut` 的使用方式，但面向硕士学位论文。

## 工作流

1. 先读取 `references/hfut-master-format.md`，确认学校规范、示例前置页顺序和正文格式。
2. 将用户给出的论文内容整理成 `example.md` 同类结构：封面/摘要/参考文献等放在 YAML frontmatter，正文用 Markdown 标题、段落、图、表表达。
3. 缺少封面元信息时先向用户确认，不要编造题目、导师、专业、研究方向、参考文献或成果清单。
4. 运行生成脚本：

```bash
python "${SKILL_DIR}/scripts/build_thesis.py" input.md output.docx
```

`SKILL_DIR` 是本技能目录，通常为 `C:\Users\a\.codex\skills\thesis-format-hfut-master`。

## 输入 Schema

最小 frontmatter 示例：

```yaml
---
unit_code: "10359"
student_id: "2023210000"
security: ""
classification: "TP391"
degree_category: "学历硕士"
title_zh: "中文题目"
title_en: "English Title"
author: "张三"
author_en: "Zhang San"
advisor_name: "李四"
advisor_title: "教授"
major: "计算机科学与技术"
research_direction: "人工智能"
complete_time: "2026年6月"
complete_month_en: "June"
complete_year_en: "2026"

defense_committee:
  chair: "专家工作单位，职称，姓名"
  members:
    - "专家工作单位，职称，姓名"
    - "专家工作单位，职称，姓名"
  advisor: "合肥工业大学，教授，李四"

graduation_destination:
  work_unit: ""
  telephone: ""
  email: ""
  address: ""
  postcode: ""

acknowledgments: |
  致谢正文。

abstract_zh: |
  中文摘要正文，建议 500-600 字。
keywords_zh: [关键词一, 关键词二, 关键词三]
abstract_en: |
  English abstract.
keywords_en: [keyword one, keyword two, keyword three]

references:
  - "马建勋，梅占馨．筒仓在地震作用下的计算理论[J]．土木工程学报，1997，30（1）：25-30．"

appendix: |
  附录1 主要符号说明

academic_achievements: |
  1）参加的学术交流与科研项目
  （1）项目名称，项目来源，起止时间
---
```

正文写法：

```markdown
# 第一章 绪论

## 1.1 研究背景

正文段落。

### 1.1.1 国内外研究现状

正文段落。

![图2.1 酶解时间对DH与ACE抑制率的影响](figures/figure-2-1.png)
Fig 2.1 Effects of enzymolysis time on the degree of hydrolysis and ACE inhibition rate

表2.1 三种肌球蛋白/多糖混合凝胶的红外光谱数据
Tab 2.1 FT-IR spectra data for three kinds of myosin-polysaccaride gel

| Treatment | PK1 | PK2 |
|---|---:|---:|
| Myosin gel | 3439 | — |
```

## 输出规范要点

- 前置页顺序：封面、中文题名页、英文内封、答辩委员签名页、独创性声明和版权使用授权书、致谢、中文摘要、英文摘要、目录、插图清单/表格清单/符号注释表（必要时）。
- 正文层级：章标题 `#`，节标题 `##`，小节标题 `###`。章标题居中黑体三号加粗；节标题黑体小四；小节标题宋体小四加粗。
- 正文段落：宋体小四，数字和字母 Times New Roman，20 磅固定行距，首行缩进 2 字符。
- 页面：A4；左右边距 3 cm；上下边距 2.54 cm。
- 图题：图片在上，中文图题和英文 Fig 题在下，居中，小五号。
- 表题：中文表题和英文 Tab 题在表格上方，居中，小五号；表格用三线表，表内五号或小五号，单倍行距。
- 参考文献：按用户给定顺序输出；不要生成不存在的文献；样式为五号，20 磅固定行距，悬挂缩进。

## 验证

生成后至少运行一次脚本烟测或打开 `.docx` 检查结构。提醒用户：Word 目录、图表清单和页码域通常需要在 Word/WPS 中“更新域”；封面下划线和签名页可能需要按学院模板微调。

## 不要做

- 不要改写用户论文观点或替用户扩写研究成果。
- 不要伪造参考文献、答辩委员、项目、论文、专利或软件著作权。
- 不要把硕士论文规则替换成本科规则；正文行距是 20 磅，不是本科示例中的 22 磅。
