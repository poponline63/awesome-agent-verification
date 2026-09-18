# Awesome Agent Verification [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

Tools and practices for deciding whether autonomous agent work is actually done: eval harnesses, LLM judges, tracing, guardrails, benchmark suites, and the discipline of writing a finish line down before the work starts.

An agent that reports success is not evidence of success. This list collects the open-source projects and practices that put a checkable claim between "the agent says it finished" and "it finished", covering the measurement half (does it work, and how do we know), the inspection half (what did it actually do), and the enforcement half (what stops it declaring victory).

## Contents

- [Eval Frameworks](#eval-frameworks)
- [LLM as a Judge](#llm-as-a-judge)
- [Benchmarks and Task Suites](#benchmarks-and-task-suites)
- [Tracing and Observability](#tracing-and-observability)
- [Guardrails and Output Validation](#guardrails-and-output-validation)
- [Data and Behaviour Assertions](#data-and-behaviour-assertions)
- [Spec and Acceptance Discipline](#spec-and-acceptance-discipline)

## Eval Frameworks

- [DeepEval](https://github.com/confident-ai/deepeval#readme) - Pytest-style evaluation for LLM output, with agent metrics and trace-level scoring.
- [promptfoo](https://github.com/promptfoo/promptfoo#readme) - Test prompts, agents and RAG pipelines against assertions, with side-by-side model comparison.
- [Inspect](https://github.com/UKGovernmentBEIS/inspect_ai#readme) - Evaluation framework for coding, reasoning and agentic tasks, built for reproducible runs.
- [OpenAI Evals](https://github.com/openai/evals#readme) - Framework and registry for evaluating models and systems against published benchmarks.
- [simple-evals](https://github.com/openai/simple-evals#readme) - Small, readable reference implementations of common evals.
- [HELM](https://github.com/stanford-crfm/helm#readme) - Holistic evaluation covering accuracy, robustness, fairness and efficiency across scenarios.
- [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness#readme) - The long-standing harness for few-shot evaluation across hundreds of academic tasks.
- [MLCommons Inference](https://github.com/mlcommons/inference#readme) - Reproducible benchmark rules and reference implementations for model serving.
- [ragas](https://github.com/vibrantlabsai/ragas#readme) - Reference-free metrics for retrieval-augmented systems, useful when no gold answer exists.

## LLM as a Judge

- [anthropics/evals](https://github.com/anthropics/evals#readme) - Worked examples of rubric and model-graded evaluation, including agentic grading.
- [llm-judge](https://github.com/motasemwed/llm-judge#readme) - Small rubric-based judge service, useful as a shape to copy rather than a dependency.

## Benchmarks and Task Suites

- [SWE-bench](https://github.com/SWE-bench/SWE-bench#readme) - Real GitHub issues resolved and graded by the repository's own test suite.
- [SWE-agent](https://github.com/SWE-agent/SWE-agent#readme) - The reference agent for SWE-bench, and the harness most issue-fixing agents are compared against.
- [tau-bench](https://github.com/sierra-research/tau-bench#readme) - Tool-agent-user interaction, graded on whether the resulting database state is correct.
- [tau2-bench](https://github.com/sierra-research/tau2-bench#readme) - The successor suite, extended to dual-control and more domains.
- [AgentBench](https://github.com/THUDM/AgentBench#readme) - Multi-environment benchmark for evaluating models as agents across eight task families.
- [WebArena](https://github.com/web-arena-x/webarena#readme) - Self-hosted web environments with functional correctness checks rather than text matching.
- [OSWorld](https://github.com/xlang-ai/OSWorld#readme) - Real operating system tasks in a VM, evaluated by executing the resulting state.
- [Terminal-Bench](https://github.com/harbor-framework/terminal-bench-1#readme) - Tasks in a terminal, graded by the state the terminal is left in.

## Tracing and Observability

- [Langfuse](https://github.com/langfuse/langfuse#readme) - Trace, score and compare agent runs, with datasets and prompt management in one platform.
- [OpenLLMetry](https://github.com/traceloop/openllmetry#readme) - OpenTelemetry instrumentation for LLM and agent applications, so runs land in existing APM tooling.
- [OpenLIT](https://github.com/openlit/openlit#readme) - OpenTelemetry-native tracing and evaluation for agents and coding agents, including cost tracking.
- [Phoenix](https://github.com/Arize-ai/phoenix#readme) - Trace visualisation and evaluation workbench, strong on diagnosing retrieval and tool failures.
- [Opik](https://github.com/comet-ml/opik#readme) - Tracing, evaluation and experiment comparison with an emphasis on debugging agent trajectories.
- [MLflow](https://github.com/mlflow/mlflow#readme) - Experiment tracking that grew into model and evaluation tracking; the durable default for run history.

## Guardrails and Output Validation

- [guardrails](https://github.com/guardrails-ai/guardrails#readme) - Schema, type and policy validation around model calls, with automatic correction loops.
- [OpenAI Guardrails](https://github.com/openai/openai-guardrails-python#readme) - Input and output guardrails wired into an agent's own lifecycle hooks through the Agents SDK.
- [Skyvern](https://github.com/Skyvern-AI/skyvern#readme) - Browser automation whose steps are verified against the page state rather than assumed from a click.

## Data and Behaviour Assertions

- [Great Expectations](https://github.com/fivetran/great_expectations#readme) - Declarative expectations for data, the clearest prior art for "state what must be true, then check it".
- [pytest](https://github.com/pytest-dev/pytest#readme) - The assertion engine most agent verification ends up running inside, with fixtures for expensive setup.
- [pre-commit](https://github.com/pre-commit/pre-commit#readme) - Hooks that make a check unavoidable at commit time instead of advisory.

## Spec and Acceptance Discipline

- [Spec Kit](https://github.com/github/spec-kit#readme) - Spec-driven development workflow for agents, from specification to tasks to implementation.
- [Agent-Proof](https://github.com/Consecutive-Gen-AI/Agent-Proof-#readme) - Independent verification of agent claims, with a tamper-evident record of what ran.
- [agent-trace](https://github.com/oleg-vdv/agent-trace#readme) - Inventory and tamper detection for agent artefacts, aimed at proving what a run actually did.

## Related Lists

- [Awesome Evals](https://github.com/benchflow-ai/awesome-evals#readme) - Papers, blogs and tools on building and evaluating agents.
- [Awesome LLM Evaluation Tools](https://github.com/danielrosehill/Awesome-AI-Evaluations-Tools#readme) - Frameworks and tools for evaluation across tool use, agentic AI and multimodal.
- [Awesome LLM Observability Tools](https://github.com/aglio-lab/llm-observability-tools#readme) - A long list of tracing, monitoring and cost platforms.

## Contributing

Contributions are welcome. Read the [contribution guidelines](CONTRIBUTING.md) first, then open a pull request.
