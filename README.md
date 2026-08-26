# Mobile Design Skills

Two portable Agent Skills for designing native mobile and wearable products:

- **`mobile-ux`** — how the experience works: flows, information architecture, navigation, interaction, states, recovery, accessibility, adaptivity, and watch capability selection.
- **`mobile-ui`** — how the experience looks and feels: visual direction, hierarchy, typography, color, spacing, materials, imagery, motion, platform expression, and anti-template critique.

The skills support iOS, iPadOS, Android phones and large screens, watchOS, and Wear OS. They follow the open Agent Skills format and are designed for any compatible agent. The [`skills` CLI](https://github.com/vercel-labs/skills) provides convenient installation across supported clients.

## Design philosophy

- Mobile is not a miniature desktop.
- Tablet is not a large phone.
- Watch is not a tiny phone.
- A watch is a selective product surface, not a feature-parity target.
- Adaptation means recomposition, not scaling.
- Cross-platform consistency does not require pixel parity.
- Native behavior does not require generic visual design.

When concerns conflict, the skills prioritize safety and data integrity, accessibility and task completion, comprehension and agency, platform conventions, product consistency, visual identity, cross-platform parity, and implementation convenience—in that order.

## Install with `npx skills`

List the available skills:

```sh
npx skills add emland89/mobile-design-skills --list
```

Install both interactively:

```sh
npx skills add emland89/mobile-design-skills
```

Install both globally for a specific agent without prompts:

```sh
npx skills add emland89/mobile-design-skills --skill mobile-ux --skill mobile-ui --global --agent <agent> --yes
```

Replace `<agent>` with the CLI identifier for your client. Repeat `--agent <agent>` to target multiple agents, or omit `--agent` to choose interactively.

Install only one skill:

```sh
npx skills add emland89/mobile-design-skills --skill mobile-ux
npx skills add emland89/mobile-design-skills --skill mobile-ui
```

You can also install from a full GitHub URL:

```sh
npx skills add https://github.com/emland89/mobile-design-skills
```

For a local checkout:

```sh
npx skills add . --list
npx skills add .
```

The skills are not tied to the CLI or to any one coding agent. If your agent supports the Agent Skills format but is not recognized by the CLI, copy either folder from `skills/` into that agent's skills directory.

## Recommended workflow

1. Use `mobile-ux` to establish the behavioral contract and select the capabilities appropriate to each form factor.
2. Use `mobile-ui` to create a distinctive, platform-appropriate visual system for that contract.
3. Use a framework-specific implementation skill for SwiftUI, Jetpack Compose, React Native, or the chosen stack.
4. Re-run UX and UI audits after implementation or screenshots are available.

## Repository layout

```text
skills/
├── mobile-ux/
│   ├── SKILL.md
│   └── references/
└── mobile-ui/
    ├── SKILL.md
    └── references/
```

The main skill files contain routing and operating guidance. Platform-specific and topic-specific detail is loaded from one-level references only when relevant.

## License

The skills are available under the [MIT License](LICENSE).
