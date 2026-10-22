# IGNIS Core Development Evidence Ledger

This public repository records cryptographic hashes for privately retained
IGNIS Core development backups. It does not contain source code, datasets,
credentials, executable bundles, or private project files.

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

