# Policy snapshot

Every DUNE software policy, its status and its owner, on one page. Each policy is a Markdown file in this repository, so a change to a policy is a pull request, reviewed like code. Where a policy has a fuller write-up (a LaTeX document in DocDB, for example), the page here summarises it and links to it; the write-up is the authoritative text.

| Policy | Status | Version | Owner | Last change |
|---|---|---|---|---|
| [Units](units.md): the CLHEP system of units, two coding rules, a units firewall around LArSoft | <span class="status ratify">For ratification</span> | 2 | Brett Viren, Gavin S. Davies | 17 Nov 2026 |
| [Dependency change control](dependency-change-control.md): how external upgrades that can change physics are accepted, validated and released | <span class="status progress">In progress</span> | | | |
| [Coding conventions](coding-conventions.md): the Phlex guidelines as the baseline, with DUNE additions | <span class="status progress">In progress</span> | | | |
| [Pull requests](pull-requests.md): what a PR must say, and what a reviewer owes the author | <span class="status progress">In progress</span> | | | |
| [Code ownership](code-ownership.md): teams, CODEOWNERS and rulesets across the DUNE organization | <span class="status progress">In progress</span> | | | |
| [AI-assisted code](ai-usage.md): guardrails and disclosure | <span class="status progress">In progress</span> | | | |

## Status meanings

| Status | Meaning |
|---|---|
| <span class="status progress">In progress</span> | Being written. A placeholder page; nothing applies yet. |
| <span class="status draft">Draft</span> | Being written. Comments welcome, nothing applies yet. |
| <span class="status proposed">Proposed</span> | Presented to the collaboration. Open for comment, or waiting for its comment period. |
| <span class="status ratify">For ratification</span> | Comments closed and answered; the revised version is in front of CRAB. |
| <span class="status adopted">Adopted</span> | Ratified by CRAB. Code that does not follow it has a bug. |

## Proposing a change

Open an issue or a pull request against the policy's page. Substantive changes to an adopted policy go through the same steps as a new one: see [How a policy changes](process.md).

!!! note "For AI tools too"
    `AGENTS.md` in each Phlex-era DUNE repository points here, so coding agents read the same rules as people.
