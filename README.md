<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="check.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">check.me.at</h1>

<p align="center"><strong>My linting conventions, one rule at a time, with the reasoning.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-171717?style=flat-square" alt="Status: in development">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#screenshots">Screenshots</a> ·
  <a href="#built-with">Built with</a>
</p>

A red lint run tells you what broke, but rarely why the rule exists. I built check.me.at to document the house conventions I enforce across ESLint, Biome and `me-at check` (my monorepo's own workspace checker). Each rule in my shared ESLint 9 flat config gets its own page with its reasoning, a before and after, and the carve-outs that keep it switched on. It is for anyone curious why my codebase is shaped the way it is, and for contributors who want the reasoning behind a failing check.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="check.me.at at a glance: one page per rule, who enforces it, grouped by what it guards, config read from source" width="880">
  </picture>
</p>

## Why check.me.at

| The usual lint config | check.me.at |
| --- | --- |
| A list of rule names and severities | A page per rule with the reasoning, examples and carve-outs |
| You guess which tool runs a rule | Each rule names the engine that enforces it in CI, or says nothing does |
| Rules in one long file | Rules grouped by the axis they protect, with counted totals |
| Docs that drift from the config | A severity matrix read from the config source at build time |

## Features

- **One page per rule**: rationale, example pairs, options, when not to use it, related rules, and version history, rendered from MDX.
- **Rules grouped by what they protect**: the index groups every rule by the axis it guards (style, TypeScript, and more), with totals counted from the rule pages themselves.
- **Who enforces it**: each rule shows which engine (the ESLint preset, Biome, or `me-at check`) actually runs it in CI, and says so plainly when nothing does.
- **Config matrix**: every rule the flat config sets and its severity in each named config block, read from the config source as text at build time.
- **The me-at check half**: an overview of the repository-wide checker, where rules read every app's manifest and need no config file.
- **The field**: a survey of the lint and format tools around the preset, showing which ones run on every pull request here.
- **Light and dark themes** across every page.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How check.me.at works: write, collect, read config, render" width="880">
  </picture>
</p>

Every rule is written as an MDX document, and content collections check each one against the same schema before the site builds. At build time the flat config source is read as text to produce the severity matrix, so the published config view cannot drift from the real one. The rule pages, the grouped index and the matrix all render from those two sources.

## Screenshots

<table>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/config-dark.png"><img src=".github/assets/config.png" alt="Config matrix"></picture><br><sub>Config matrix: every rule and its severity per config block.</sub></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/rules--kebab-case-filenames-dark.png"><img src=".github/assets/rules--kebab-case-filenames.png" alt="kebab-case-filenames rule page"></picture><br><sub>kebab-case-filenames: a house rule and who enforces it.</sub></td>
  </tr>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/rules--func-style-dark.png"><img src=".github/assets/rules--func-style.png" alt="func-style rule page"></picture><br><sub>func-style: the rationale for arrow-function expressions.</sub></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/rules--consistent-type-definitions-dark.png"><img src=".github/assets/rules--consistent-type-definitions.png" alt="consistent-type-definitions rule page"></picture><br><sub>consistent-type-definitions: type aliases over interfaces.</sub></td>
  </tr>
</table>

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/MDX-rule%20docs-525252?style=flat-square&logo=mdx&logoColor=white" alt="MDX rule documents">
  <img src="https://img.shields.io/badge/ESLint-9-737373?style=flat-square&logo=eslint&logoColor=white" alt="ESLint 9">
  <img src="https://img.shields.io/badge/Biome-lint-737373?style=flat-square&logo=biome&logoColor=white" alt="Biome">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- MDX rule documents through content collections
- ESLint 9 flat config, Biome

## Part of the me.at family

check.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
