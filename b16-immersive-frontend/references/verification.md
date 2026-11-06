# Verification checklist

Tailor this checklist to the authorized scope and record evidence, not assumptions.

## Structure and content

- Semantic hierarchy, landmarks, links, buttons, forms, labels, and real copy are intact.
- No placeholder, fabricated proof, unauthorized brand mark, copied identity, or unlicensed asset remains.
- One icon family is used consistently; exceptions are official brand marks or documented functional needs.

## Responsive visual review

- Capture and inspect at least one representative mobile viewport and one desktop viewport.
- Check first viewport, longest copy, navigation, forms, final CTA, footer, overflow, crops, line length, and safe areas.
- Inspect loading, empty, error, disabled, active, selected, focus, and success states that exist in the flow.

## Interaction and access

- Complete the primary path with keyboard and visible focus.
- Verify touch and coarse-pointer behavior; nothing essential depends on hover.
- Confirm focus is not trapped or displaced by pinning, transforms, overlays, or route transitions.
- Confirm accessible names stay intact when text is visually split.
- Confirm reduced motion produces stable final states without scrub, parallax, autoplay, smooth scroll, or continuous canvas animation.

## Motion and rendering

- Compare each implemented animation to its contract: purpose, trigger, duration, mobile behavior, and fallback.
- Test interruption, repeated entry, resize, orientation change, background tab, and cleanup where relevant.
- Verify static poster and WebGL failure path. Check context loss when feasible.
- Confirm canvas pauses offscreen/hidden, DPR is capped, resources dispose, and no duplicate animation loop or observer remains.

## Performance

- Run the project's available build, lint, type, and test commands when authorized.
- Measure the agreed performance budget with an appropriate browser/device profile.
- Inspect bundle additions, media dimensions/compression, font loading, layout shift, long tasks, and frame stability.
- Record environment, viewport, device emulation, command, result, and limitations.

## Handoff statement

Report four separate categories:

1. Automated checks actually run.
2. Visual and interaction checks actually performed.
3. Evidence paths or screenshots.
4. Remaining risks and unverified conditions.
