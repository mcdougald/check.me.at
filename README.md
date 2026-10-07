<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="check.me.at landing page" width="880">
  </picture>
</p>

# check.me.at

Linting conventions, hosted by me.

check.me.at documents the house conventions enforced across ESLint, Biome, and `me-at check` (the monorepo's own workspace checker). Each rule in the shared ESLint 9 flat config gets its own page with its reasoning, a before and after, and the carve-outs that keep it switched on. It is for anyone curious why a codebase is shaped the way it is, and for contributors who want the reasoning behind a red lint run.

## Features

- **One page per rule**: rationale, example pairs, options, when not to use it, related rules, and version history, rendered from MDX.
- **Rules grouped by what they protect**: the index groups every rule by the axis it guards (style, TypeScript, and more), with totals counted from the rule pages themselves.
- **Who enforces it**: each rule shows which engine (the ESLint preset, Biome, or `me-at check`) actually runs it in CI, and says so plainly when nothing does.
- **Config matrix**: every rule the flat config sets and its severity in each named config block, read from the config source as text at build time.
- **The me-at check half**: an overview of the repository-wide checker, where rules read every app's manifest and need no config file.
- **The field**: a survey of the lint and format tools around the preset, showing which ones run on every pull request here.
- **Light and dark themes** across every page.

## Screenshots

<table>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/config-dark.png"><img src=".github/assets/config.png" alt="Config matrix"></picture><br><sub>Config matrix: every rule and its severity per config block</sub></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/rules--kebab-case-filenames-dark.png"><img src=".github/assets/rules--kebab-case-filenames.png" alt="kebab-case-filenames rule page"></picture><br><sub>kebab-case-filenames: a house rule and who enforces it</sub></td>
  </tr>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/rules--func-style-dark.png"><img src=".github/assets/rules--func-style.png" alt="func-style rule page"></picture><br><sub>func-style: rationale for arrow-function expressions</sub></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/rules--consistent-type-definitions-dark.png"><img src=".github/assets/rules--consistent-type-definitions.png" alt="consistent-type-definitions rule page"></picture><br><sub>consistent-type-definitions: type aliases over interfaces</sub></td>
  </tr>
</table>

## Built with

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- MDX rule documents through content collections
- ESLint 9 flat config, Biome

## Part of the me.at family

check.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

See [LICENSE](LICENSE).
