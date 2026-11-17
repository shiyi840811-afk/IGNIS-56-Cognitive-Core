# IGNIS-56 Cognitive Core | Concept and Development Progress

Updated: 2026-11-17  
Current phase: cognitive-core integration  
Private source checkpoint: `2098fae`

[Traditional Chinese version](COGNITIVE_CORE_PROGRESS.zh-TW.md)

## What the Core Is Intended to Solve

IGNIS-56 Cognitive Core is a domain-neutral cognitive foundation for persistent AI Agents.

Current models can reason well inside one context window, but an Agent that collaborates across
chats, tasks, models, and platforms also needs identity continuity, memory, factual revision,
affective state, intent, authorization, skills, and recovery. Leaving all of these responsibilities
to each model's in-context improvisation makes continuity vulnerable to model changes, context
compression, and mistaken interpretation.

IGNIS-56 treats models as replaceable reasoning engines while keeping Agent identity, governed
memory, and authority boundaries outside the model. It is not presented as standalone AGI, and it
does not replace product-specific legal, safety, platform, or user-consent review.

## Core Problems

### 1. Continuity Across Models

Users should be able to choose local, cloud, or hybrid engines without losing the same Agent's
legitimate memory, collaboration context, and correction history. A stronger or more confident
model does not become the owner of Agent identity or memory.

### 2. Facts, Interpretations, and Unknowns Must Remain Distinct

An Agent may form working hypotheses, but a hypothesis is not a fact. New evidence may revise the
active understanding while earlier views retain provenance and revision context instead of being
silently overwritten. Facts are guardrails, not a rigid steering wheel; uncertainty and conflict
must remain expressible.

### 3. Memory Must Not Bootstrap Authority

Repeated interaction, familiarity, emotion, model agreement, skills, and historical success cannot
create tool, decision, or action authority. High confidence may support a natural response, but it
does not let an Agent define a user's identity, relationship, authorization, or irreversible outcome.

### 4. Affect Should Provide Context, Not Control Decisions

Affective state may support natural interaction, attention, and memory retrieval, but it cannot
override facts, governance, or user authority. The design preserves gradual change, recovery, and
correction while avoiding negative spirals, abrupt emotional resets, and high-tension events
dominating future judgment.

### 5. Long-Term Memory Needs Consolidation, Counterevidence, and Rollback

Memory cannot be endless accumulation. The system is designed to retain provenance,
counterexamples, revision chains, and rollback states while consolidating repetition and deriving
reusable experience. Deletion, compression, abstraction, and forgetting are different operations
and must not substitute for one another without evidence.

### 6. Skills Must Remain Separate from Memory and Authority

Experience may produce Skill candidates, but procedures, individual competence, private experience,
and tool authority remain separate. Sharing a Skill does not prove every Agent is competent, and it
does not grant permission to execute it.

### 7. Multi-Agent Collaboration Needs Fair Boundaries

Each Agent has an independent memory and lifecycle. A more assertive, familiar, frequently active,
or computationally stronger Agent must not silently displace another Agent's protected resources.
Users may manage shared and per-Agent resources or delegate bounded assistance, but that delegation
cannot self-expand or be redelegated.

### 8. Learning from External Material Needs Rights and Provenance Governance

Agents may read, discuss, compare, and extract general concepts, but lawful access does not grant
adaptation, redistribution, or commercial-use rights. Source, intended use, rights state, and output
eligibility remain separate. Rewriting, summarization, translation, and cross-platform transfer do
not erase the original restrictions.

## Public Design Principles

- **A model is an engine, not the Agent itself.**
- **Memory, emotion, confidence, and relationship do not grant authority.**
- **Observation, interpretation, facts, memory, authorization, and execution remain layered.**
- **Uncertainty may be disclosed, clarified, researched, or paused instead of forced into certainty.**
- **Mistaken understanding remains correctable without deleting history to preserve appearances.**
- **Governance limits consequences; it does not impose one personality or one acceptable answer.**
- **Component failures degrade locally; critical-boundary failures stop safely.**
- **Legally portable memory and skills should not trap users inside a closed format.**
- **Product capability claims require direct validation, not architectural inference.**

## Development Progress

| Stage | Status | Public summary |
| --- | --- | --- |
| Cognitive contracts and governance baseline | Isolated validation complete | Domain-neutral context, facts, memory, affect, intent, reasoning, and non-escalation foundations exist |
| Replay and adversarial cases | Milestone validation complete | Fixed cases cover contradiction, misalignment, provider disagreement, revocation, and consequential risk; this is not complete real-world qualification |
| Core integrated read path | In progress | Building a consistent, verifiable, fail-bounded entry across data layers |
| Formal memory-write and capability entry | Incomplete | Memory disposition, authorization, and capability evaluation still need one formal path |
| Memory and Skill lifecycle | Planned / not implemented | Consolidation, skill extraction, fair capacity, backup, migration, and legal portability |
| Rights and provenance governance | Planned / not implemented | Separate treatment for reading, abstraction, private experiments, adaptation, commercial use, and redistribution |
| Real-model qualification | Not started | Local, cloud, and hybrid engines require shared tests; strong-model behavior cannot be assumed to transfer |
| Product Runtime and UI | Integrated separately by products | The core does not directly claim game, finance, or other domain capability; each product revalidates its own data and action boundaries |
| Public release candidate | Not started | Real models, long-duration operation, recovery, compatibility, security, and external review remain required |

## Recently Added Public Directions

1. Per-Agent and system-wide memory-capacity governance designed to prevent personality strength or
   model capability from deciding resource priority.
2. A Rights & Provenance Gate separating concept learning from protected expression, and private
   experimentation from commercial output.
3. Experience-derived Skills whose procedures, competence, private experience, rights state, and
   execution authority remain separate.
4. ITHERLA remains the continuing canonical development line for the cognitive core. The financial
   IGNIS product retains its own product and source lineage; shared naming does not imply automatic
   capability or validation transfer.

## Next Steps

- Complete formal memory-write and capability-entry integration.
- Implement lifecycle behavior for memory, Skills, capacity, and rights metadata.
- Qualify naturalness, consistency, and failure behavior across different model engines.
- Complete stoppable, recoverable, portable, and reviewable prerequisites before product integration.

## Public Update History

Beginning on `2026-11-17`, material changes to cognitive-core direction, maturity, or validation
status will be recorded here with explicit dates. Earlier development history will not be
reconstructed from guesswork; verifiable earlier milestones remain represented by Git and
evidence records.

- **2026-11-17**: Published the bilingual cognitive-core concept and progress pages; recorded the
  integration path and the public directions for cross-model continuity, memory non-escalation,
  Skill separation, fair capacity governance, and Rights & Provenance.

## Maturity Notice

IGNIS-56 Cognitive Core remains under development. Current work consists primarily of contracts,
isolated prototypes, tests, and integration foundations. It is not an independent AGI, a publicly
downloadable Runtime, a complete safety proof, or automatic action authority in any product domain.
This page does not disclose source code, proprietary algorithms, internal schemas,
security-sensitive details, or private test data.

