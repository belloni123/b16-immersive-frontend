# Stack selection

Choose the smallest tool that expresses the approved idea without imposing a new application architecture.

## Decision order

1. Can semantic HTML and CSS express it with acceptable behavior and performance?
2. Can the project's existing animation system handle it coherently?
3. Does the interaction need a timeline, scroll coordination, canvas throughput, or a 3D scene?
4. Is the added runtime, maintenance, accessibility, and fallback cost justified?
5. Has installation been explicitly authorized?

## Tool roles

- CSS and Web Animations API: small transitions, state feedback, simple entrances, and native view transitions.
- Motion: component-level layout, enter/exit, gesture, and orchestration in supported JavaScript frameworks.
- GSAP and ScrollTrigger: controlled timelines, sequencing, pinning, and justified scroll-linked narratives. Keep one owner per animated property and refresh measurements after fonts or media change.
- Lenis: optional scroll smoothing when native scroll cannot achieve an approved narrative. Use at most one smooth-scroll engine, bypass it for reduced motion, and verify keyboard, anchors, focus, touch, and cleanup.
- Three.js: direct control of a purposeful WebGL scene, shader, or spatial interaction.
- React Three Fiber and selective drei helpers: declarative Three.js within an existing React project. Do not introduce React solely to use it.
- PixiJS: sprite-heavy, filter-heavy, or high-throughput 2D canvas experiences where DOM/SVG is insufficient.

## Example choices

### WordPress landing page

Default to semantic Elementor or theme markup, CSS, and small scoped JavaScript. Add GSAP/ScrollTrigger only for an approved sequence that CSS cannot express. Keep the CTA and content independent of motion. Do not add React for a decorative effect.

### React marketing site

Use the existing React stack. Prefer CSS or Motion for component behavior. Add GSAP for a deliberate cross-section timeline. Use dynamic loading for heavy scenes and keep the semantic page complete before they load.

### 3D hero

Use a compressed static poster as the first frame and fallback. Choose Three.js directly for a focused scene or React Three Fiber when React already exists and its lifecycle/composition benefits are material. Define device thresholds, capped DPR, loading state, context-loss behavior, pause rules, disposal, and reduced-motion replacement before building.

## Rejection signals

Reject or simplify a proposed tool when it duplicates an existing system, requires a framework migration for one effect, makes essential content canvas-only, lacks a credible static fallback, depends on hover, obscures focus or scroll behavior, exceeds the budget, or cannot be maintained by the project team.
