# IGNIS-56 Cognitive Core - Development Evidence Ledger

This public repository records cryptographic hashes for privately retained
IGNIS-56 Cognitive Core development backups. It does not contain source code, datasets,
credentials, executable bundles, or private project files.

## Project overview

IGNIS-56 is a local-first cognitive core for persistent AI agents. Its purpose
is to help an agent preserve identity and continuity across sessions, tasks,
and replaceable model providers while working with people over time.

At a high level, the core helps an agent organize context, memory, emotional
state, uncertainty, permissions, and tool use into one coherent operating
continuity. It is intended to support agents that can recall relevant
experience, revise prior understanding when evidence changes, retain a
recognizable personality, and distinguish a plausible interpretation from an
authorized action.

IGNIS-56 is designed for collaboration rather than unchecked autonomy. Human
authority, explicit boundaries, traceable state, and safe stopping behavior
remain part of the operating model. Confidence or emotion alone does not grant
permission, and an agent should be able to ask, defer, refuse, or return control
when the available context or authority is insufficient.

The core is model-agnostic and may support local models, cloud platforms, or a
hybrid of both without making one provider the permanent owner of the agent's
identity and memory. It is also intended to remain reusable across different
product domains rather than being tied to a single application.

Detailed architecture, algorithms, governance contracts, implementation
choices, datasets, and source code remain private during development.

## Purpose

Each evidence record binds a local Git bundle and tracked-source snapshot to a
public GitHub commit. A retained artifact can later be checked by recomputing
its SHA-256 digest and comparing it with the corresponding record.

## Verification

1. Obtain the privately retained artifact named in an evidence record.
2. Compute its SHA-256 digest with a trusted implementation.
3. Compare the result with the recorded digest.
4. For Git bundles, also run `git bundle verify <bundle>` and inspect the
   recorded Git HEAD and tree identifiers.

## Evidence limits

Publication supports a claim that the exact retained artifact existed no later
than the public record. It does not independently prove authorship,
originality, software correctness, commercial rights, or an immutable trusted
timestamp. Git author and committer dates are development metadata and can be
rewritten by a repository owner.

The private artifacts must therefore remain preserved separately. This ledger
contains hashes only and cannot reconstruct the underlying source code.

