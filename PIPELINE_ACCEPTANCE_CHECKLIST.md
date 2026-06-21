# Aperospec Pipeline Acceptance Checklist

## 1. Council Readiness（会议讨论就绪度）
*用于评估当前草稿是否足够拿给人类讨论*
- 输入已被 Runtime 正确拆解。
- 涉及的各 Skill 已经基于职责给出了专业意见。
- 形成了结构完整的 Team Synthesis Brief。
- 明确列出了 Unresolved Questions 和需要人类决策的关键点。

## 2. Production Readiness（生产就绪度）
*用于评估当前方案是否已经被人类确认并可以冻结生产*
- 用户已经明确下达“方案定稿 / 可以正式生产”的确认指令。
- 认知层、叙事层、页面层、视觉层的核心蓝图已经进入 Locked 状态。
- 没有遗留的、会阻断流水线的基础矛盾。
- Runtime 可以顺利启动正式 CWP -> NWP -> CDP -> VDP 链条。

### External Research Readiness

Before moving from Council Mode to Production Mode, Runtime must check whether any unresolved factual, market, cultural, policy, technical, case-study, or visual-reference assumptions require external research.

The pipeline is production-ready only if one of the following is true:

- no external research is needed;
- required external research has been completed and synthesized;
- the human explicitly decides to proceed without external research;
- unresolved research items are marked as non-blocking.

External research must not silently alter locked content, user intent, or final production direction.
### Final Output Format Confirmed

Before Production Mode begins, Runtime must confirm the final output format with the human.

The final output format must be explicitly recorded.

If the format is still undecided, the pipeline is not production-ready.

The system must not infer or default to a format based on prior wording such as "deck", "slide", "visual campaign", or "final output".
