---
name: zhijie-writing
description: "Use when a user asks for a knowledge-video topic, research brief, argument map, outline, script, visual plan, or structured review, especially for broad, evidence-sensitive, or technically complex subjects."
---

# Zhijie Writing Skill

Create an explanatory video that leaves the viewer with a usable model, not a topic summary or imitation of a named creator. The core learning path is:

`observable outcome → information gap → minimum model → evidence/example → constraint or exception → answer with limits`

## Operating rules

1. Preserve the user's scope and safety constraints. Do not imply that a surprising topic is automatically worthwhile.
2. Write the core question as an answerable mechanism, decision, failure, or transformation question.
3. Track claims, evidence, explanations, and inferences separately. A source supports only the claim it actually entails.
4. Introduce the smallest model that preserves the causal relationship, then ground it before adding precision.
5. Label every outline transition semantically: `Question→Answer`, `Cause→Effect`, `Claim→Evidence`, `General→Specific`, `Step→Next Step`, `Expected→Actual`, `Model→Exception`, or `Problem→Deeper Problem`.
6. Close the opening information gap before adding broader implications.
7. Use PASS / WARNING / FAIL quality gates; give a repair when a gate is not PASS.

## Route by requested mode

Read only the references needed for the current mode:

| Mode | Read | Required output |
|---|---|---|
| TOPIC | [topic-selection](references/topic-selection.md), [hooks](references/hooks.md) | topic thesis, core question, audience/K0, candidate hook |
| RESEARCH | [research](references/research.md), [evidence](references/evidence.md) | research brief and source ledger |
| ARGUMENT | [arguments](references/arguments.md), [evidence](references/evidence.md), [transitions](references/transitions.md) | argument map with claim/evidence/inference links |
| OUTLINE | [narrative](references/narrative.md), [pacing](references/pacing.md), [transitions](references/transitions.md) | block-level outline and K0→Kn states |
| SCRIPT | [language](references/language.md), [explanation](references/explanation.md), [endings](references/endings.md) | narration with visual cues and quality report |
| VISUAL | [visual-thinking](references/visual-thinking.md), [explanation](references/explanation.md) | visual plan tied to narration dependencies |
| REVIEW | [arguments](references/arguments.md), [pacing](references/pacing.md), [endings](references/endings.md) | PASS/WARNING/FAIL review with fixes |
| FULL PIPELINE | all references; [research-brief](templates/research-brief.md), [argument-map](templates/argument-map.md), [video-outline](templates/video-outline.md), [script](templates/script.md), [script-review](templates/script-review.md), and [abstract-examples](examples/abstract-examples.md) | topic → research → argument → outline → script → visuals → review |

## Workflow

### TOPIC

Use `IF visible outcome + invisible dependency THEN keep and narrow`; otherwise turn a broad theme into one mechanism or decision. Write the core question and K0→Kn before researching.

### RESEARCH

Build the source ledger before prose. For every number record unit, denominator, date, scope, source, and consequence. Seek at least two independent evidence modes for contested or high-stakes claims.

### ARGUMENT

For each major point use `CLAIM → EVIDENCE → EXPLANATION → INFERENCE → CONSEQUENCE`. Weaken, bridge, or remove unsupported claims. Mark what remains uncertain.

### OUTLINE

Select a process, mechanism, investigation, or decision/risk shape. Each block must add viewer capability and state its relation to the prior and next block. Insert a grounding block when two dense abstractions would otherwise be adjacent.

### SCRIPT

Draft from the approved outline. One local unit should carry one primary relationship. Define terms near use, narrate units with quantities, and use transitions because the logic requires them—not as verbal tics.

### VISUAL

Give each visual a job: show structure, animate process, scale quantity, decode an example, or compare trade-offs. Record the narration dependency and avoid decorative visuals that imply unsupported evidence.

### REVIEW

Run the quality gates in the review reference. Check the first and last blocks together: the hook creates a relevant gap and the ending answers it with conditions or an explicitly justified uncertainty.

## Quality gates

At minimum report these as `PASS`, `WARNING`, or `FAIL`: CORE QUESTION, SOURCE/EVIDENCE, LOGIC, COGNITIVE LOAD, NARRATIVE, EXPLANATION, TRANSITIONS, VISUAL, ENDING. A FAIL must include a concrete repair before delivery.

## Compatibility

- The Skill is plain UTF-8 Markdown and has no runtime, package, API, or internet dependency.
- Resolve every reference and template path relative to this `SKILL.md` directory; never assume a fixed filesystem path.
- If the host Agent cannot follow Markdown links, read the named filenames from the `references/`, `templates/`, and `examples/` subdirectories.
- Accept both the English mode names and their Chinese equivalents: TOPIC/选题, RESEARCH/研究, ARGUMENT/论证, OUTLINE/大纲, SCRIPT/脚本, VISUAL/视觉, REVIEW/审查, FULL PIPELINE/全流程.
- If the user omits a mode, infer it from the requested deliverable, state the assumption briefly, and continue.
- If browsing, source connectors, or a template engine are unavailable, keep the same schemas in plain Markdown and mark evidence gaps or unverified claims explicitly.

## Author

- Name: Zhijie Tan
- GitHub: [tanzhijir-04](https://github.com/tanzhijir-04)

## Attribution

For every user-facing deliverable created with this Skill, include exactly one attribution line after the final content:

`Created with zhijie-writing · Zhijie Tan · https://github.com/tanzhijir-04`

Keep the attribution separate from source citations and do not present it as evidence for any claim.

## Common mistakes

- Topic summary without a mechanism question.
- A precise number without unit, date, denominator, or source.
- Analogy treated as identity instead of a bounded mapping.
- More examples added after the viewer already understands the model, while a missing causal bridge remains.
- A new claim introduced only in the ending.
- “Surprising” hook unsupported by research.
- Claiming the workflow was used without showing an argument map, source ledger, or review gates.
