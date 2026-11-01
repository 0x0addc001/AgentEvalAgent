# AgentEvalAgent

**An Agent that turns evaluation into a closed-loop control system for an Agent-native stack.**

AgentEvalAgent defines falsifiable claims, designs adversarial probes, verifies trajectories and scores, explains verdicts, and routes every failure to the upstream owner.

用 Agent 托管评测闭环：定义可证伪命题、设计对抗探针、验证轨迹与分数、解释裁决，并把失败准确回写到上游责任环节。

## Agent loop

| Stage | Responsibility |
|---|---|
| Data | Benchmarks, traces, failure slices, rubrics, adversarial sets |
| Model | Systems under test, judge models, and reward-model audits |
| Training | Checkpoint comparisons and regression slicing |
| Inference | Online canaries, A/B tests, latency and cost probes |
| Harness | Evaluation runners, sandboxes, telemetry, and report generation |
| Eval | Pass rate, robustness, calibration, regressions, and evaluation cost |

## System contract

- Treat every score as a claim with traceable evidence.
- Keep deterministic checks separate from model judges.
- Route failures to data, model, training, inference, or harness owners.

## Engineering principles

- Design tests to break assumptions.
- Calibrate judges and audit contamination.
- Verify closure after upstream repairs.

