# Mobile Gameplay UX Review

An agent skill for reviewing mobile web games through Playwright playtesting. Compare desktop keyboard controls with touch-enabled mobile emulation and produce actionable UX findings without changing application code.

## Install

```sh
npx skills add three-fourteen/mobile-gameplay-ux-review --skill mobile-gameplay-ux-review
```

## Use

Ask your agent:

> Use mobile-gameplay-ux-review to test this web game with Playwright and produce mobile-gameplay-review.md with prioritized findings and measurable acceptance criteria.

Provide the game URL or repository, local startup instructions, and relevant gameplay requirements. The environment needs Playwright and a browser engine (Chromium initially; WebKit optionally).

## Review coverage

- Desktop gameplay baseline and multiple mobile gameplay sessions
- Touch controls, rapid direction changes, input timing, and control visibility
- Browser interaction conflicts that emulation can reproduce
- Reproduction steps, player impact, evidence, severity, and acceptance criteria

## Output

`mobile-gameplay-review.md` includes the test environment, desktop baseline, mobile assessment, ranked findings, implementation priorities, validation plan, and limitations.

Playwright device emulation does not verify physical touch latency, thumb comfort, or native mobile browser gestures. Unsupported checks must be documented as unverified. Application code is modified only when explicitly requested.

The skill is in `skills/mobile-gameplay-ux-review/SKILL.md`. The optional `.codex-plugin` manifest packages the same skill for Codex.
