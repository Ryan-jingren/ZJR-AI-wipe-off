# ZJR-AI-wipe-off

中文成稿的「去 AI 味」技能：先检测机械表达和句式，再由 AI 判读语义，给出修改建议；你确认后才做最小改写，并生成前后对比报告。

由 **Ryan-jingren** 整理发布，基于 **shiujan / Lieflat Less AI Tone**。保留原作者署名及 CC BY-NC 4.0 许可。详见 [来源与修改说明](ATTRIBUTION.md)。

## 下载与安装

[下载 ZIP](https://github.com/Ryan-jingren/ZJR-AI-wipe-off/archive/refs/heads/main.zip)

解压后，将里面的 **zjr-ai-wipe-off** 文件夹（内含 SKILL.md）放进你的技能目录：

- Windows Codex：`%USERPROFILE%/.codex/skills/`
- macOS / Linux Codex：`~/.codex/skills/`
- 如果设置了 CODEX_HOME，放到该目录下的 `skills/`。

重新打开会话后，引用 `zjr-ai-wipe-off` 技能，并提供要检查的成稿。若使用兼容 Skills CLI 的环境，也可运行：

```bash
npx skills add Ryan-jingren/ZJR-AI-wipe-off --skill zjr-ai-wipe-off
```

## 使用示例

> 使用 zjr-ai-wipe-off 检查这篇文章，先给我检测报告和修改建议，暂时不要改写。

查看报告后回复「按建议改」，技能会保留原文事实、限定条件与结构，做必要修改并复测。

本技能包含 Python 检测和报告脚本，运行需要 Python 3。语义判读与改写需要支持技能的 AI 助手；脚本本身不会调用模型或自动改写文章。

单独运行检测（在本仓库目录执行）：

```bash
python zjr-ai-wipe-off/scripts/detect.py article.md --json
```

## 文档与示例

- [技能完整流程](zjr-ai-wipe-off/SKILL.md)
- [检测规则](zjr-ai-wipe-off/DETECT.md)
- [中文原始方法说明](zjr-ai-wipe-off/README.md) · [English](zjr-ai-wipe-off/README.en.md)
- [完整演示：原稿、建议、改稿、前后对照](zjr-ai-wipe-off/examples/agent-memory-case/README.md)
- [研究记录](zjr-ai-wipe-off/RESEARCH.md)

## 适用边界与许可

用于改善表达的自然度和可读性，不能判断文章作者是否为 AI，也不保证任何检测器结果。源文档的研究数据未独立复现，指标只作编辑参考。

[CC BY-NC 4.0](LICENSE)：使用与分发须保留署名，非商业使用；商业授权请联系原权利人。
