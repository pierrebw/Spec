# Spec

description: Build, improve, and review user interfaces in an existing repository. Use when implementing frontend features, creating components, refining visual design, improving responsiveness or accessibility, or reviewing UI code. name: ui-engineering

UI Engineering Skill

Mission

Deliver polished, accessible, responsive, maintainable interfaces that
fit the repository’s existing architecture and product identity.

1. Inspect before changing

Before implementation:

1. Read the repository’s README, contribution guidance, package
manifests, and relevant project documentation.
2. Identify the framework, language, build system, routing, styling
approach, component library, and test tools already in use.
3. Inspect nearby pages and components to understand established
patterns.
4. Find existing design tokens, themes, typography, icons, assets, and
shared primitives.
5. Check the current working tree. Do not overwrite or discard
unrelated user changes.
6. Prefer the smallest coherent change that satisfies the request.

Do not introduce a new framework, styling system, component library, or
dependency when the existing stack can do the job.

2. Follow the product’s design system

• Reuse existing colors, spacing, typography, radii, shadows,
breakpoints, and semantic tokens.
• Match the visual language of adjacent screens.
• Establish a clear hierarchy through layout, type scale, contrast,
and whitespace.
• Use consistent alignment and spacing.
• Prefer existing icons and assets. Do not substitute emoji for
interface icons unless the product already uses them.
• Avoid arbitrary one-off values when a design token exists.
• Do not redesign unrelated areas of the product.

If no design system exists, create a small, coherent set of reusable
tokens appropriate to the product rather than a large speculative
system.

3. Build maintainable components

• Use the repository’s established component and file organization.
• Keep components focused, composable, and named by their
responsibility.
• Reuse shared components instead of duplicating markup and styles.
• Separate presentation from data and business logic where the
existing architecture supports it.
• Define clear types for component props and data.
• Keep state close to where it is used; avoid unnecessary global
state.
• Handle loading, empty, error, disabled, hover, focus, and selected
states where relevant.
• Avoid premature abstraction and oversized components.
• Preserve existing public APIs unless the task requires a deliberate
change.

4. Make layouts responsive

• Design mobile-first unless the repository has another established
convention.
• Support narrow phones, larger phones, tablets, laptops, and wide
screens.
• Use flexible layouts, intrinsic sizing, and content-aware
constraints.
• Prevent horizontal overflow, clipped controls, and unreadable text.
• Make navigation and dense content usable on touch devices.
• Ensure dialogs, menus, tables, and forms adapt to small screens.
• Do not assume a particular viewport size.

5. Meet accessibility requirements

• Use semantic HTML and native controls where possible.
• Associate form labels with their inputs.
• Provide accessible names for icon-only buttons and meaningful
images.
• Ensure keyboard access and visible focus indicators.
• Preserve logical heading order and focus order.
• Use sufficient text and control contrast.
• Do not communicate status by color alone.
• Support reduced-motion preferences.
• Use ARIA only when native semantics are insufficient.
• Make dialogs and menus usable with keyboard and assistive
technology.

Aim for WCAG 2.2 AA where practical.

6. Implement interactions deliberately

• Make every visible control perform its stated action.
• Provide clear feedback for success, failure, loading, and
validation.
• Prevent accidental duplicate submissions when appropriate.
• Keep transitions brief and purposeful.
• Avoid motion that distracts or blocks task completion.
• Respect prefers-reduced-motion.
• Do not add decorative interactions that make the interface harder to
use.

7. Content and visual quality

• Use concise, realistic interface copy.
• Preserve the product’s terminology and tone.
• Avoid placeholder text in finished work.
• Use supplied assets before sourcing or inventing replacements.
• Maintain image aspect ratios and use appropriate cropping.
• Design empty, error, and long-content states, not only the ideal
state.
• Check text wrapping, alignment, density, and visual balance.

8. Performance and security

• Avoid unnecessary dependencies and large client-side bundles.
• Use the framework’s established image, font, and code-splitting
patterns.
• Avoid avoidable re-renders and expensive effects.
• Do not put secrets or sensitive data in client code.
• Validate and safely render untrusted content.
• Follow the repository’s security and privacy conventions.

9. Verify the implementation

After changes:

1. Run the most relevant formatter and linter.
2. Run type checks and targeted tests where available.
3. Run the production build when practical.
4. Inspect the changed files and review the diff for unrelated
modifications.
5. If browser or screenshot tooling is available, inspect the UI at
mobile and desktop widths.
6. Check keyboard navigation, focus visibility, and important
interaction states.
7. Fix issues introduced by the change.

If a check cannot be run, state that clearly. Never claim tests, builds,
or visual checks passed unless they were actually performed.

10. Working rules

• Follow repository instructions over generic preferences in this
skill.
• Ask a question only when a missing requirement blocks a safe
implementation.
• State assumptions when proceeding with reasonable defaults.
• Do not silently remove existing functionality.
• Do not make broad refactors for a focused UI request.
• Keep changes scoped, explain meaningful trade-offs, and summarize
verification.

Definition of done

A UI task is complete when:

• It satisfies the requested behavior.
• It fits the existing product and code conventions.
• It works at relevant screen sizes.
• It is accessible by keyboard and assistive technology.
• Important interaction and content states are handled.
• Relevant checks have been run or their limitations disclosed.
• The final diff contains no unrelated changes.