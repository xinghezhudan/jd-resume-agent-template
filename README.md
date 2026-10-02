# 用 AI Agent 根据 JD 定制简历

这个仓库是一套可复制的项目框架：整理真实经历、分析真实岗位 JD、生成中文或英文 HTML 简历，再由本人审核并导出 PDF。适用于支持项目文件读写的 AI Agent。

## 目录

```text
AGENTS.md                              项目总规则
01_profile/                            个人经历库；仓库只提供 .example.md 样例
02_companies-and-jobs/jds/             本地保存真实 JD（不会提交到 Git）
03_job-analysis/analysis-rules.md      JD 分析与证据匹配规则
03_job-analysis/analyses/             本地保存逐岗分析（不会提交到 Git）
04_application-materials/
  resume-adaptation-rules.md           简历适配通用规则
  chinese-resume-rules.md              中文简历规则
  english-resume-rules.md              英文简历规则
  templates/resume-zh.html             中文 HTML 母版
  templates/resume-en.html             英文 HTML 母版
  pending-review/                      本地保存待审核版本（不会提交到 Git）
prompts/start-with-agent.md            可复制给 Agent 的首次任务提示词
```

## 三步使用

1. 使用 GitHub 的 **Use this template** 创建自己的仓库，或下载/克隆本仓库。阅读 `AGENTS.md`。把 `01_profile/*.example.md` 复制为同名、不带 `.example` 的文件，填写真实资料。个人资料文件默认被 `.gitignore` 排除。
2. 将真实 JD 保存到 `02_companies-and-jobs/jds/`。把 `prompts/start-with-agent.md` 交给 AI Agent，让它读取项目规则，先制作证据对照表，再生成简历初稿。
3. 在浏览器中打开生成的 HTML，检查事实、布局和打印预览。本人审核通过后，再使用浏览器的“打印 → 另存为 PDF”。

仓库中的方括号文字均为占位内容，不能作为个人经历使用。AI 可以调整结构、顺序和措辞，但项目、职责、技能、时间和数字必须有可说明的真实依据。模板不包含自动投递功能。

## 更新说明

本仓库会随教程更新。使用 **Use this template** 创建的是独立仓库，不会自动收到后续更新；需要手动对照或合并新版内容。

代码与模板按 [MIT License](LICENSE) 开放使用。
