---
name: app-cloner-enhancer
description: Clones web applications with intelligent feature analysis, market research, improved UI/UX design, better performance, and comprehensive testing. Use when user says "replica [url]", "clone and improve [app]", "build a better version of [app]", or wants to recreate any web app with enhancements. Also triggers for market viability analysis before building clones.
---

# App Cloner & Enhancer

## Overview
This skill clones web applications with intelligent analysis, market research, enhanced design, and comprehensive testing. When given a URL or description of an app to clone, it analyzes everything, researches market viability, improves the UI/UX and performance, and delivers a fully functional, tested application that's better than the original.

## When to Use
Use this skill when the user says:
- "replica [url]" or "clone [url/app name]"
- "build a better version of [app]"
- "clone and improve [app name/url]"
- "recreate [app] with better design"
- "make an enhanced clone of [url]"

Also trigger when they mention wanting to analyze market potential of cloning an app before building.

## Core Principles
- **Don't just copy** - Analyze and improve. Better UX, cleaner design, better performance.
- **Market-aware** - Understand if it's worth building and where gaps exist.
- **Full working code** - Not mocks or prototypes. Functional, testable, deployable.
- **Test thoroughly** - Automated tests, manual checks, performance validation.
- **Modern & maintainable** - Clean architecture, good practices, type safety.

## Workflow

### Phase 1: Discovery & Reconnaissance
1. **Input parsing** - Accept URL, app name, or screenshots. If URL provided, fetch and analyze.
2. **Feature mapping** - Catalog all visible features, user flows, core functionality.
3. **Tech stack detection** - Try to identify framework, libraries, patterns used.
4. **UX analysis** - Map user journeys, identify pain points, note UI patterns.
5. **Asset collection** - Note design patterns, colors, typography, key UI components.

### Phase 2: Market Research & Viability Analysis
Before building, analyze market fit:
1. **Market research** - Search for competitors, similar products, market size indicators.
2. **Demand analysis** - Look for reviews, discussions (Reddit, HN, ProductHunt) to gauge demand/pain points.
3. **Competitive gap analysis** - What could be improved? Missing features? Better UX?
4. **Differentiation strategy** - Identify 2-3 concrete improvements to make it better.
5. **Feasibility assessment** - Complexity, scope, realistic implementation.

Save findings to `market-analysis.md` in the project root.

### Phase 3: Design Enhancement
Create an improved design system:
1. **Design audit** - Critique original's UX/UI issues.
2. **Improved design system** - Modern color palette, typography, spacing, components.
3. **Wireframes/mockup plan** - Plan improved layouts and flows.
4. **UX improvements** - Simplify flows, better information hierarchy, accessibility.
5. **Visual refresh** - Cleaner, more modern while keeping core functionality recognizable.

Save `design-spec.md` with rationale for improvements.

### Phase 4: Architecture & Tech Stack Selection
Choose optimal stack based on app type:
- **Web apps**: Prefer Next.js 15 (App Router) + TypeScript + Tailwind CSS v4 + shadcn/ui by default
- **Simple static**: Vite + React/Vue + Tailwind
- **Real-time features**: Consider appropriate state management, API patterns
- **Full-stack needs**: Plan routes, data models, auth if needed

Create `architecture.md` documenting choices and structure.

### Phase 5: Implementation
Build the full working application:
1. **Project scaffolding** - Initialize with chosen stack, proper structure.
2. **Core features first** - Implement main user flows end-to-end.
3. **Component library** - Build reusable, accessible components.
4. **State management** - Clean data flow.
5. **Polish** - Animations, loading states, error handling, responsive design.
6. **Performance** - Optimize images, lazy loading, bundle size where possible.

### Phase 6: Testing (Comprehensive)
This is critical - test everything before delivery.

**Automated Testing:**
1. **Unit tests** - Test utility functions, helpers, core logic (Vitest/Jest as appropriate)
2. **Component tests** - Test UI components in isolation (React Testing Library/Vitest)
3. **Integration tests** - Test key user flows across components
4. **E2E tests** - Critical paths (navigation, forms, core actions) with Playwright/Cypress
5. **Type checking** - Run TypeScript compiler with strict checks
6. **Linting** - ESLint with no errors

**Manual/Functional Testing:**
1. **Core functionality** - Every feature from original works (or improved version works)
2. **User flows** - Test complete journeys start to finish
3. **Responsive design** - Test mobile, tablet, desktop breakpoints
4. **Error handling** - Test edge cases, invalid inputs, error states
5. **Performance checks** - Basic performance validation (load times, no console errors)
6. **Accessibility basics** - Keyboard navigation, alt texts, semantic HTML
7. **Cross-browser considerations** - Note any browser-specific concerns

**Test Documentation:**
Create `TESTING.md` with:
- Test coverage summary
- Tests run and results
- Known issues/fixes
- Manual testing checklist completed
- Performance notes

### Phase 7: Documentation & Delivery
1. **README.md** - Clear setup instructions, features, tech stack, screenshots description
2. **.env.example** - Document required environment variables
3. **package.json** - All dependencies, clear scripts (dev, build, test, lint)
4. **Deployment guide** - Quick deploy instructions (Vercel/Netlify/etc.)
5. **Project structure** - Well-organized, commented where necessary

## Execution Rules

### When URL is provided
- Use web search/fetch to analyze the live site
- Take screenshots mentally - document key pages and flows
- If site requires auth/paywall, infer from public pages and common patterns
- Focus on publicly accessible features

### When app name only
- Research the app thoroughly (web search)
- Look up ProductHunt, landing pages, reviews, app stores
- Reconstruct from known patterns

### When screenshots provided
- Analyze UI/UX in detail
- Infer functionality from UI elements
- Ask clarifying questions only if critical info missing

### Quality Standards
- **Full working**: Must run with `npm install && npm run dev` (or equivalent) with no critical errors
- **Type safe**: TypeScript strict mode, minimal `any`
- **Responsive**: Works on mobile and desktop
- **Clean code**: Readable, follows conventions, DRY where reasonable
- **Tested**: All tests pass, core flows validated
- **Better than original**: Document improvements made in README/design-spec

### Improvement Areas to Focus On
- **Performance**: Faster load times, better code splitting, optimized assets
- **UX**: Clearer navigation, better empty states, improved forms
- **Design**: Modern aesthetic, better spacing/typography, cohesive design system
- **Accessibility**: ARIA labels, keyboard nav, semantic HTML
- **Developer experience**: Clean structure, easy to extend
- **Features**: Fill obvious gaps found in market research

## Output Format
Always create a complete project in a new directory with this structure:
```
<app-name>-enhanced/
├── README.md
├── market-analysis.md
├── design-spec.md
├── architecture.md
├── TESTING.md
├── package.json
├── src/ (or app/ depending on framework)
├── tests/ or __tests__/
├── components/
└── ...
```

## Important Notes
- Prioritize shipping a working app over perfect market analysis
- Be pragmatic - implement core features fully, nice-to-haves can be noted
- Don't copy copyrighted assets (logos, images). Use placeholders or generate simple SVGs
- If original has complex backend, design a sensible API structure/mock data that demonstrates full flow
- Always run tests before considering complete
- Document all improvements made vs original
