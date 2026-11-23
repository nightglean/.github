<div align="center">

<img src="../assets/nightglean-lockup.png" width="720" alt="Nightglean Studio" />

# Nightglean Studio

**Independent studio · native implementations · ask "can this be done without it?" first**

A very small independent studio building Android apps and engineering experiments.
No framework chasing, no dependency stacking — every build step stays something we can read and explain ourselves.
Founded in November 2026 by [Wang Sunyang](https://github.com/wang-sunyang), who remains its sole founder, sole owner and final decision-maker. Copyright in the studio's work and its marks stays with him personally; the organization holds no ownership, only permission to host.

[![Android](https://img.shields.io/badge/Android-5.0%2B-3DDC84?logo=android&logoColor=white)](https://github.com/nightglean)
[![No Gradle](https://img.shields.io/badge/build-no%20Gradle-1f6feb)](https://github.com/nightglean)
[![License](https://img.shields.io/badge/license-MIT-2ea44f)](https://github.com/nightglean)
[![Website](https://img.shields.io/badge/site-nightglean.github.io-c2a878)](https://nightglean.github.io/)

**English** · [简体中文](README.zh-CN.md)

</div>

---

### Projects

| Project | What it is | Technical stance | Status |
| --- | --- | --- | --- |
| **OneStar**<br>[wang-sunyang/onestar](https://github.com/wang-sunyang/onestar) | A "daily star" journal: one mood entry a day, accumulating into a hand-drawn star map, with a home-screen widget, a mood curve and a year-in-review poster | Plain Java + hand-drawn Canvas, no Gradle / no AndroidX / no third-party SDK; `aapt2 + javac + d8 + apksigner` wired by hand, JNI layer built with `zig cc` | 0.12.x in progress, targetSdk 37 |
| **AppFunction Guard**<br>[wang-sunyang/appfunction-guard](https://github.com/wang-sunyang/appfunction-guard) | Android 16's `AppFunctions` let AI agents call functions inside an app; this library adds the per-function authorization, rate limiting, argument validation and audit trail the platform leaves out | Kotlin 2.2, `minSdk 26`, MIT; one interception point between platform and business logic | alpha |
| **moltdisk**<br>[wang-sunyang/moltdisk](https://github.com/wang-sunyang/moltdisk) | A disk check-up tool: finds build artifacts that can be rebuilt from source (`node_modules`, `target`, `dist`, `venv`, `Pods`), measures them, ranks them, and shows the evidence for "why this is deletable". It deletes nothing itself | Rust 2021, MSRV 1.80, MIT; no deletion code path at all, `-y` is an error | v0.1.0 |
| **Marvis · Persona Spec**<br>[wang-sunyang/marvis-persona-spec](https://github.com/wang-sunyang/marvis-persona-spec) | A persona spec that a program can check: 30 dialogue slots, 20 banned phrases, a runnable lint script, 10 benchmark cases, plus the Fault Bloom visual system | Python lint + Markdown spec; two-stage adoption in CI, from grey-scale report to a hard gate | v3 |

> All six repositories are still maintained under the personal account ([wang-sunyang](https://github.com/wang-sunyang)) — [onestar](https://github.com/wang-sunyang/onestar), [appfunction-guard](https://github.com/wang-sunyang/appfunction-guard), [moltdisk](https://github.com/wang-sunyang/moltdisk), [marvis-persona-spec](https://github.com/wang-sunyang/marvis-persona-spec), and two further projects that are not public yet — and will move here only after two conditions are met: a tagged release that has been publicly available for at least one release cycle, and at least three external contributions that completed the full issue → PR → review → merge loop. Where a project carries its own governance file, that file states these conditions in §1.1. The criteria live in each repository, not on this page; this page only records that they exist. The two projects that are not public yet are left unnamed here on purpose. The `.github` repository of this organization only carries this profile and the brand assets.

### Founder and ownership

| Question | Answer |
| --- | --- |
| Who founded this organization | [Wang Sunyang](https://github.com/wang-sunyang), November 2026 |
| Who owns it | The same person — the organization has exactly one owner, no pending owner invitations |
| Who owns the code and the marks | The person, never the organization; see [AUTHORS.md](../AUTHORS.md) and [TRADEMARK.md](../TRADEMARK.md) |
| Who decides | The founder, as stated in each project's `GOVERNANCE.md` — reserved powers cannot be amended away by a later vote |

An owner account in an organization can add or remove other owners; that is a platform
mechanism, not a governance one. This organization is kept at a single owner on purpose,
and any future co-owner is introduced by a written amendment to `GOVERNANCE.md` first,
never the other way round.

### Visuals

<div align="center">

<img src="../assets/nightglean-poster.png" width="360" alt="Nightglean · bamboo-slip poster" />

<sub>Four bamboo slips: characters carved at the centre of each slip, aligned along the seams. The horizontal lockup is for document headers, the square mark for avatars and icons.</sub>

</div>

Dark backgrounds are the default: this studio builds its things at night. The identity is four bamboo slips with a fixed seam width; glyphs are redrawn in the spirit of Chu-state script, and the visual centre of the four characters sits on one horizontal line.

### How we work

- **Native first**: screens are drawn frame by frame on a Canvas, never wrapped in a WebView — speed never bought at the cost of control.
- **Dependency restraint**: if it is one line to write, it is not worth a package. Every link in the build chain must be explainable.
- **Reproducible**: the command line produces the same APK; the build does not rely on an IDE's implicit magic.
- **Honest documentation**: READMEs record limits, pitfalls and known issues, not just highlights.

### Recently

| Area | What happened |
| --- | --- |
| OneStar 0.12.x | targetSdk raised to 37, signing and release path hardened, 16 KB page alignment re-checked, large-screen orientation guard |
| moltdisk 0.1.0 | First stable release: audit report, `why` subcommand and its evidence chain; deletion capability was removed entirely before release |
| Marvis Persona Spec v3 | Persona matrix, banned-phrase table and lint gate came together, wired into CI for grey-scale observation |
| Engineering docs | Build rules, release checklist and cross-platform conventions keep filling in |

### Build status

| Repository | Workflow | Status |
| --- | --- | --- |
| onestar | `android.yml` | [![build](https://img.shields.io/github/actions/workflow/status/wang-sunyang/onestar/android.yml?branch=main&label=build)](https://github.com/wang-sunyang/onestar/actions/workflows/android.yml) |
| onestar | `regression.yml` | [![regression](https://img.shields.io/github/actions/workflow/status/wang-sunyang/onestar/regression.yml?branch=main&label=regression)](https://github.com/wang-sunyang/onestar/actions/workflows/regression.yml) |
| appfunction-guard | `build.yml` | [![build](https://img.shields.io/github/actions/workflow/status/wang-sunyang/appfunction-guard/build.yml?branch=main&label=build)](https://github.com/wang-sunyang/appfunction-guard/actions/workflows/build.yml) |
| moltdisk | `ci.yml` | [![ci](https://img.shields.io/github/actions/workflow/status/wang-sunyang/moltdisk/ci.yml?branch=main&label=ci)](https://github.com/wang-sunyang/moltdisk/actions/workflows/ci.yml) |
| marvis-persona-spec | `persona-lint.yml` | [![lint](https://img.shields.io/github/actions/workflow/status/wang-sunyang/marvis-persona-spec/persona-lint.yml?branch=main&label=lint)](https://github.com/wang-sunyang/marvis-persona-spec/actions/workflows/persona-lint.yml) |

### Links

- Studio site: [nightglean.github.io](https://nightglean.github.io/)
- Author: [wang-sunyang](https://github.com/wang-sunyang)
- Personal site: [wang-sunyang.github.io](https://wang-sunyang.github.io)
- Questions and ideas: open an issue in the relevant repository

<div align="center">
<sub>nightglean studio — small tools, hand-built.</sub>
</div>
