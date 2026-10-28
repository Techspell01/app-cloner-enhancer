# App Cloner & Enhancer

A Claude skill that clones web applications with intelligent analysis, market research, enhanced UI/UX design, better performance, and comprehensive testing.

## Features

- **Intelligent Reconnaissance** - Analyzes target apps by URL, name, or screenshots to map features and user flows
- **Market Research & Viability** - Researches competitors, finds user pain points, identifies improvement opportunities
- **Design Enhancement** - Creates modern design systems with better UX, accessibility, and visual polish
- **Smart Tech Stack Selection** - Recommends optimal modern stacks (Next.js, TypeScript, Tailwind CSS, shadcn/ui)
- **Full Working Implementation** - Builds complete, functional apps ready to run with `npm install && npm run dev`
- **Comprehensive Testing** - Includes unit, component, integration, and E2E tests plus manual QA checklists
- **Performance Focused** - Optimized for speed, responsiveness, and clean architecture

## Usage

After installing this skill in Claude:

```
replica https://example.com
```

Or:
```
clone and improve [app name]
build a better version of [app name]
```

The skill will:
1. Analyze the target app and map its features
2. Conduct market research to find gaps and opportunities
3. Create an enhanced design with improvements
4. Build a full working app with better UI/UX and performance
5. Run comprehensive tests and generate documentation

## Output

For each clone, it creates a complete project with:
- `README.md` - Setup instructions and features
- `market-analysis.md` - Competitor analysis and opportunities
- `design-spec.md` - Design improvements and rationale
- `architecture.md` - Tech stack and structure
- `TESTING.md` - Test results and QA checklist
- Full source code with tests

## Installation

### As a Claude Skill
Download `app-cloner-enhancer.skill` from [releases](https://github.com/Techspell01/app-cloner-enhancer/releases) and install it in Claude.

### Manual Installation
Clone this repo to your Claude skills directory:
```bash
git clone https://github.com/Techspell01/app-cloner-enhancer.git ~/.claude/skills/app-cloner-enhancer
```

## Philosophy

This skill doesn't just copy - it analyzes, improves, and delivers apps that are genuinely better than the originals through smarter UX, cleaner design, better performance, and addressing real user pain points found through market research.

## License

MIT
