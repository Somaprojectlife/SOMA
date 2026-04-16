# Contributing to SOMA Project

> **"We just want to save lives and help the world."**

Thank you for your interest in contributing to SOMA — the open-source human body sandbox for biomedical simulation. This document explains how you can help, regardless of your background.

---

## Table of Contents

- [Who Can Contribute](#who-can-contribute)
- [Ways to Contribute](#ways-to-contribute)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Code Standards](#code-standards)
- [Community & Communication](#community--communication)
- [Code of Conduct](#code-of-conduct)

---

## Who Can Contribute

SOMA sits at the intersection of virtually every field of knowledge. **You do not need to be a programmer** to contribute meaningfully.

| Background | How You Help |
|---|---|
| 🧬 **Biologists & Physiologists** | Validate simulation models, contribute cellular/organ data |
| 🩺 **Doctors & Clinicians** | Review medical accuracy, contribute clinical parameters |
| 💻 **Software Engineers** | Build platform features, APIs, infrastructure, simulation engine |
| 📊 **Data Scientists** | Process genomic datasets, build predictive models |
| ⚛️ **Mathematicians & Physicists** | Translate biological processes into differential equations |
| 🎨 **Designers & Communicators** | Create scientific visualizations, anatomical illustrations, docs |
| 🌍 **Translators** | Localize the platform into more languages |
| ⚖️ **Bioethicists & Lawyers** | Guide ethical frameworks and intellectual property |
| 📚 **Educators** | Write tutorials, explanations, onboarding materials |
| 🤷 **Anyone Curious** | Report bugs, suggest improvements, spread the word |

---

## Ways to Contribute

### 🐛 Report Bugs
Found something broken? Open an [issue](https://github.com/Somaprojectlife/issues) with:
- A clear description of what happened
- Steps to reproduce
- Expected vs actual behavior
- Browser/OS if relevant

### 💡 Suggest Features or Improvements
Have an idea? Open a [discussion](https://github.com/Somaprojectlife/discussions) or issue tagged `enhancement`. Explain:
- What problem it solves
- Who benefits
- Any prior art or references

### 📝 Improve Documentation
Docs are often the most impactful contribution. This includes:
- Fixing typos or unclear explanations
- Adding examples
- Translating content
- Writing scientific references

### 🧪 Contribute Scientific Data
- Physiological parameter sets (normal ranges, pathological states)
- DNA/genomic profiles for different population groups
- Pharmacokinetic/pharmacodynamic models
- Validated disease progression curves

### 💻 Contribute Code
- Simulation engine modules (body systems)
- Frontend components
- APIs and data pipelines
- Performance improvements
- Test coverage

---

## Getting Started

### 1. Fork & Clone

```bash
# Fork via GitHub UI, then:
git clone https://github.com/YOUR-USERNAME/soma-project.git
cd soma-project
```

### 2. Create a Branch

Use a descriptive branch name:

```bash
# For features:
git checkout -b feat/immunological-system-cytokine-model

# For bug fixes:
git checkout -b fix/dna-profile-rendering

# For docs:
git checkout -b docs/contributing-guide
```

### 3. Make Your Changes

Keep changes focused. One branch = one concern.

### 4. Commit Clearly

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add cytokine cascade model to immunological system
fix: correct ACE2 receptor binding affinity calculation
docs: add physiological parameter reference for cardiovascular module
data: add DNA_EU_v5.9 haplogroup profile
refactor: optimize viral replication loop performance
```

### 5. Open a Pull Request

- Fill out the PR template completely
- Link to any related issues (`Closes #42`)
- Add screenshots or data validation if relevant
- Be responsive to review comments

---

## Development Workflow

### Branch Strategy

| Branch | Purpose |
|---|---|
| `main` | Stable, production-ready code |
| `develop` | Active development, integration branch |
| `feat/*` | New features |
| `fix/*` | Bug fixes |
| `docs/*` | Documentation only |
| `data/*` | New biological datasets or models |
| `experiment/*` | Research-grade, not production-ready |

### Pull Request Checklist

Before submitting, confirm:

- [ ] Code follows project style guidelines
- [ ] Changes are documented (inline + relevant README/docs)
- [ ] Tests pass (if applicable)
- [ ] No sensitive data is included (patient data, private keys)
- [ ] Scientific claims cite peer-reviewed sources
- [ ] Physiological models include validation references

---

## Code Standards

### General Principles

- **Clarity over cleverness** — code is read more than it is written
- **Document the why, not the what** — explain intent, not mechanics
- **No magic numbers** — biological constants must be named and sourced

### Scientific Accuracy

All physiological models must:
- Reference peer-reviewed literature (PubMed, WHO, established textbooks)
- State assumptions and simplifications explicitly
- Include units in variable names where ambiguous (`concentrationMgPerL` not `c`)
- Define normal ranges and pathological thresholds

```js
// ✅ Good
const ACE2_BINDING_AFFINITY_KD_NM = 0.7; // Kd in nM — doi:10.1038/s41586-020-2180-5
const IL6_NORMAL_RANGE_PG_ML = { min: 0, max: 7 }; // Sproston & Ashworth, 2018

// ❌ Avoid
const kd = 0.7;
const il6 = { min: 0, max: 7 };
```

### Commit Message Format

```
<type>(<scope>): <short summary>

[optional body — what and why]

[optional footer — breaking changes, closes #issue]
```

Types: `feat`, `fix`, `docs`, `data`, `refactor`, `test`, `chore`, `perf`

Scopes: `engine`, `cardiovascular`, `respiratory`, `immunological`, `dna`, `api`, `ui`, `i18n`, `data`

---

## Scientific Contribution Guidelines

### Adding a Body System Module

Each body system module should include:

1. **Specification document** — what it models, what it doesn't
2. **Parameter file** — all constants with units and sources
3. **Validation report** — comparison with known physiological responses
4. **Edge cases** — documented failure modes and boundary conditions

### Adding a DNA/Genomic Profile

Profiles must:
- Be derived from public datasets (1000 Genomes, gnomAD, etc.)
- Be anonymized and aggregated — **no individual-level data**
- Include population frequency metadata
- Document relevant pharmacogenomic variants

### Adding a Pathogen Model

Include:
- Taxonomy and classification
- Replication mechanism (RNA/DNA, tropism, entry receptor)
- Key virulence factors
- Published R₀ and generation time estimates
- Known treatment sensitivities

---

## Community & Communication

| Channel | Purpose |
|---|---|
| [GitHub Issues](https://github.com/Somaprojectlife/issues) | Bugs, feature requests |
| [GitHub Discussions](https://github.com/Somaprojectlife/discussions) | Ideas, questions, collaboration |
| [Discord](https://discord.gg/KSPW6NWP) | Real-time chat, community |
| [hello@somaproject.life](mailto:hello@somaproject.life) | Direct contact |

### Response Times

We are a small team. Please allow:
- **Issues**: up to 7 days for initial response
- **Pull Requests**: up to 14 days for review
- **Complex scientific PRs**: may require external peer review

### Recognition

All contributors are recognized in:
- `CONTRIBUTORS.md` (automatically updated)
- Release notes for significant contributions
- The SOMA Project website

---

## Code of Conduct

SOMA is built on a simple principle: **science and collaboration serve everyone**.

We are committed to a harassment-free environment regardless of:
- Background, experience, or education
- Gender, race, nationality, religion
- Disability or health status
- Scientific discipline or specialty

**Expected behavior:**
- Be respectful and constructive in all interactions
- Cite sources and acknowledge uncertainty
- Separate critique of ideas from critique of people
- Welcome newcomers — expertise is not a prerequisite

**Unacceptable behavior:**
- Harassment, discrimination, or personal attacks
- Misrepresenting scientific consensus
- Fabricating or manipulating data
- Using contributions to promote commercial interests

Violations can be reported to [hello@somaproject.life](mailto:hello@somaproject.life). All reports are handled confidentially.

---

## License

By contributing to SOMA, you agree that your contributions will be licensed under the same license as the project. See [LICENSE](./LICENSE) for details.

SOMA is non-profit, open-source, and exists solely to advance biomedical science for the benefit of all humanity.

---

<div align="center">

**Every contribution — code, data, documentation, or feedback — brings us closer to a world where no disease goes untreated for lack of tools.**

[⭐ Star on GitHub](https://github.com/Somaprojectlife) · [💬 Join Discord](https://discord.gg/KSPW6NWP) · [🌐 somaproject.life](https://somaproject.life)

</div>
