<div align="center">

# DrawOffer 求职提示词库

**简历诊断、JD 匹配、STAR 改写、面试准备与复盘 · 复制即用**

基于事实写简历：只用你的真实经历，不编造数字和职责。

<p>
  <a href="./LICENSE"><img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-3f6fd8?style=flat-square"></a>
  <a href="https://www.drawoffer.com"><img alt="DrawOffer 职绘" src="https://img.shields.io/badge/在线体验-drawoffer.com-3f6fd8?style=flat-square"></a>
</p>

<p>
  <a href="https://www.drawoffer.com"><strong>在线体验</strong></a> ·
  <a href="#提示词一览">提示词一览</a> ·
  <a href="#怎么用">怎么用</a> ·
  <a href="https://github.com/ql-link/drawoffer-skills">Claude Code 版</a>
</p>

</div>

---

这是 [DrawOffer 职绘](https://www.drawoffer.com) 在产品里使用的简历写作方法，整理成 8 个可以直接复制使用的提示词。不需要安装任何东西，粘贴到 ChatGPT、DeepSeek、Kimi、通义千问、豆包或 Claude 里就能用。

## 和其他简历提示词有什么不同

很多简历提示词会让 AI 把经历写得"更亮眼"，结果是凭空多出百分比、把"参与"写成"主导"，面试一追问就露馅。这套提示词每一个都内置同一组**事实底线**：

- **只用事实**：结论只建立在简历原文、你提供的岗位描述和资料、你在对话里补充的事实上。
- **不编造**：不替你补公司业务、团队规模、技术细节或数字。没有数据就写可核实的交付物，比如上线状态、覆盖范围、被谁使用。
- **不升级职责**：参与、协助不会被改成主导、负责。
- **缺什么就问**：缺少关键事实时，AI 会问你一个具体问题，而不是自己补；需要你补充的地方用【待补充】标出。
- **有原文依据**：每条建议都指出是哪一处原文、为什么是问题、怎么改，不写"建议量化""可以更突出"这类空话。

## 提示词一览

### 简历

| 提示词 | 用来做什么 |
|---|---|
| [简历诊断](./prompts/resume-diagnosis.md) | 从招聘方和面试官两个视角找出最先要改的三到五处，每条附改写示例 |
| [岗位 JD 匹配分析](./prompts/jd-resume-match.md) | 逐项对照岗位要求，找出"有但没写出来"的经历，给出三处优先补强 |
| [经历 STAR 重写](./prompts/experience-star-rewrite.md) | 按 STAR 重组一段实习或项目经历，按价值排序 bullet |
| [简历句子润色](./prompts/resume-polish.md) | 只改一句话或一条 bullet，换掉空泛动词 |
| [零基础写第一份简历](./prompts/first-resume-guide.md) | 一问一答，带应届生从零写出第一版 |
| [简历中译英](./prompts/resume-translation.md) | 保真翻译整份简历，不改写、不升级职责 |

### 面试

| 提示词 | 用来做什么 |
|---|---|
| [面试准备与追问预测](./prompts/interview-prep.md) | 预测最容易被深挖的三个位置和追问链，准备 STAR 回答和反问清单 |
| [面试复盘](./prompts/interview-review.md) | 根据你的面试记录逐题找缺口，给出下一次怎么答 |

## 怎么用

1. 打开上面任意一个提示词，复制"提示词"一节代码块里的全部内容。
2. 在 AI 助手里新开一个对话，把它作为第一条消息发出去（支持系统提示词的工具，粘贴到系统提示词里效果更好）。
3. 接着发你的简历全文，以及需要的话附上岗位 JD。

建议用新对话：之前的对话内容可能会干扰 AI 对规则的理解。

### 示例

```text
[粘贴「简历诊断」提示词]

这是我的简历，我想投后端开发实习：
[粘贴简历全文]
```

AI 会先给一句总体判断，再列出三到五条按影响排序的发现，每条都带原文位置、问题原因和改写示例。

## 在 Claude Code 里用

如果你用 Claude Code，可以直接装 [DrawOffer Skills](https://github.com/ql-link/drawoffer-skills)，它包含同一套方法，装好后说"帮我看看简历"就会自动触发：

```text
/plugin marketplace add ql-link/drawoffer-skills
/plugin install drawoffer@drawoffer-skills
```

## 需要简历模板？

[drawoffer-chinese-resume-templates](https://github.com/ql-link/drawoffer-chinese-resume-templates) 收录了 57 套免费中文简历模板，覆盖校招、实习、社招，每套都有预览图和示例数据。

## 不想每次复制粘贴简历？

[drawoffer-mcp](https://github.com/ql-link/drawoffer-mcp)让 Claude、Cursor 等 AI 工具直接读取你在 DrawOffer 里的简历和岗位，提示词里引用简历时不用再手动粘贴。

## 想要完整的产品体验？

这些提示词只负责"怎么写"。[DrawOffer 职绘](https://www.drawoffer.com) 在此基础上提供：

- 导入 PDF / Word / Markdown 简历，自动识别模块后直接编辑；
- 中文简历模板与排版，导出 A4 分页或智能一页 PDF；
- 按岗位 JD 改简历，每处修改由你确认后才写入；
- AI 模拟面试与复盘、求职进度看板。

简历编辑、导出和岗位看板免费使用。

## 参与贡献

欢迎提 Issue 和 PR：某个提示词在某个模型上效果不好、规则有漏洞，或者你有更好的写法，都可以提出来。修改时请保持"只用事实、不编造、不升级职责"这几条底线。

## 许可证

[MIT](./LICENSE) © 2026 ql-link

部分写法改编自 [HireTechUpUp/resume-agent-prompts](https://github.com/HireTechUpUp/resume-agent-prompts)（MIT），详见 [THIRD_PARTY_NOTICES.md](./THIRD_PARTY_NOTICES.md)。
