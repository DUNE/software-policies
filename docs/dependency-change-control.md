# Dependency change control

<span class="status ratify">For ratification</span> · Owners: Tom Junk, Gavin S. Davies

How DUNE accepts, validates and releases changes to external software that can change physics results. Presented to CRAB and at the September 2026 collaboration meeting. Formal adoption is still to be confirmed.

!!! note "Key steps only"
    This page records the steps of the approved process. A fuller write-up will follow and will be linked here.

## Scope

- **In:** Geant4, GENIE, CORSIKA, ROOT; the framework stack (art and LArSoft, then Phlex and FORM); compilers and language standards; ML libraries used in reconstruction.
- **Out:** DUNE's own code (normal review and CI), patch releases with no API or physics change, and local developer environments.

## Lifecycle

1. **Request for change.** A GitHub issue from a template, opened by a convener or software lead: versions, physics motivation, urgency and deadlines.
2. **Initial review, within two weeks.** The Global Software Technical Lead accepts, defers or rejects it, with written reasons. Acceptance means "worth pursuing", not a release date.
3. **Validation.** The physics group owns it: CI, key distributions, CPU and memory, convener sign-off.
4. **Comment period, two weeks.** So no affected group is surprised.
5. **Release.** Final approval; the Release Manager integrates the change.

Analysis coordinators and affected conveners are consulted on the record. They are not co-approvers. No upgrade that changes physics output goes in during an active production campaign unless it is an emergency.

## Emergency track

Security and critical fixes are assessed within 48 hours, with reduced validation and no comment period. A full report follows within 30 days.

## Records

Requests are kept as closed GitHub issues. The Technical Lead keeps a register of approved versions.
