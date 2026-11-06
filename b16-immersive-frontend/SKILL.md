---
name: b16-immersive-frontend
description: Plan, art-direct, implement, or review distinctive motion-rich and 3D web experiences when immersion materially supports the brief. Use for cinematic heroes, scroll narratives, WebGL, interactive portfolios, premium launches, or explicit immersive frontend requests; do not invoke for ordinary UI work or as a replacement for the B16 Dev OS workflow.
---

# B16 Immersive Frontend

Create a memorable experience around one defensible visual idea. This skill complements a broader project workflow; it does not replace governance, planning, build, verification, or review skills and does not claim to reproduce B16 Dev OS.

## Establish the brief

Digest all available context before asking questions. Infer facts only when evidence supports them, cite the source or label the inference, and ask only for gaps that can materially change the direction. Use [briefing.md](references/briefing.md) when the direction is not already approved.

Before implementation, present a compact direction covering the visual thesis, content hierarchy, hero focal point, typography, palette, layout rhythm, motion narrative, likely stack, performance budget, fallbacks, asset provenance, and exclusions. Obtain approval for this direction. Do not treat approval of a concept as permission for deployment, purchases, accounts, tokens, or unrelated system changes.

## Design with intent

- Start mobile first, then expand composition and choreography for larger viewports.
- Ground the identity in the subject, audience, materials, language, and real content. Avoid a generic component-kit look.
- Spend visual boldness in one memorable place and keep the supporting system disciplined.
- Write human, technically accurate copy in active voice. Use sentence case and no em dash punctuation. Never invent proof, partners, testimonials, metrics, or capabilities.
- Use one coherent icon family per project, chosen for stack fit, identity, coverage, license, cost, maintenance, accessibility, and weight. Use official or authorized brand marks. Import individual icons with real tree shaking where the stack supports it.
- Make every primary action operable without hover. Specify touch, keyboard, focus, active, loading, disabled, error, and empty states where relevant.

## Choose the smallest sufficient stack

Read [stack-selection.md](references/stack-selection.md) when motion, 2D canvas, or 3D is under consideration. Preserve the current stack unless a change is justified and approved.

Do not add React to WordPress for one effect. Do not make any library mandatory across sites. Do not install a dependency merely because it appears in a plan. Prefer CSS and platform APIs for simple transitions, Motion for component choreography, GSAP with ScrollTrigger for deliberate timeline or scroll sequences, PixiJS for demanding 2D scenes, Three.js for direct WebGL, and React Three Fiber with selective drei helpers when React already exists and declarative scene composition is beneficial. Lenis is optional, never automatic.

Use ReactBits and Codrops only as selective references. Confirm the license and provenance of code and assets before reuse. Prefer original synthesis; preserve required notices for any licensed excerpt.

## Specify motion before building it

For every meaningful animation, record:

1. Purpose: what it explains, prioritizes, confirms, or makes spatially legible.
2. Trigger: load, entry, click, state change, pointer, scroll, or media progress.
3. Duration and easing: include limits for repetition and interruption.
4. Mobile behavior: what changes for viewport, coarse pointer, touch, battery, and device capability.
5. Fallback: final static state for reduced motion, unavailable JavaScript, failed media, lost WebGL, or constrained hardware.

Avoid hover-only meaning and decorative continuous motion. Navigation, primary message, and CTA must work before animation completes. Under `prefers-reduced-motion: reduce`, render stable final states and remove scrubbed, parallax, autoplay, or smooth-scroll behavior rather than only shortening it.

## Budget performance

Set measurable budgets appropriate to the project before implementation. Consider initial JavaScript, media weight, font count, animation concurrency, long tasks, layout shift, largest-content timing, frame stability, GPU memory, device-pixel ratio, and thermal cost.

For canvas or WebGL, provide a static poster; cap pixel ratio; pause when offscreen or hidden; avoid per-frame allocation; reduce work on small or constrained devices; handle context failure; and dispose frames, observers, listeners, textures, geometries, materials, render targets, and renderer state. Semantic content and controls must remain outside or independent of the canvas.

## Implement proportionally

Preserve the approved direction and existing project conventions. Keep semantic HTML and real content as the source of truth. Load heavy experiences only where they add value. Scope effects so multiple systems do not control the same property. Use a single smooth-scroll engine at most, and only when its value outweighs the complexity.

Do not install libraries, modify a project, or implement before the plan is approved. When implementation is authorized, explain any stack or asset addition before making it and respect the project's package manager and lockfile.

## Verify honestly

Use [verification.md](references/verification.md) for implementation or review work. Inspect mobile and desktop screenshots, interaction states, touch, keyboard, focus, reduced motion, static fallbacks, loading and failure behavior, performance evidence, and cleanup behavior in proportion to the change.

Report exactly what ran, what passed, what was inspected visually, and what remains unverified. Never imply that a build, browser test, accessibility check, device test, or performance measurement ran when it did not.

## Reference provenance

The guidance is an original synthesis. Consult [sources.md](references/sources.md) for authoritative documentation and clearly labeled community inspiration. Do not install or execute third-party skill code through this skill.
