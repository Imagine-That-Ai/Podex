# Design System — Po"Codex

## Product Context

- **What this is:** A visual and product home for a custom Codex CLIProxy companion layer: remote control, isolated account seats, runtime state, and launch ceremony.
- **Who it's for:** One operator moving between Codex accounts, machines, and remote execution targets who needs the truth of the connection state to stay legible.
- **Space/industry:** Developer tooling and local AI runtime operations.
- **Project type:** Marketing surface now; operational desktop surface next.

## Aesthetic Direction

- **Direction:** Industrial-refined with a small amount of orbital wit.
- **Decoration level:** Intentional. Use real imagery, a little texture, and a few animated marks; keep routine controls quiet.
- **Mood:** Warm, precise, and slightly ceremonial. The interface should feel like a well-made instrument, not a generic SaaS dashboard.
- **Reference cues:** Grok-D's sense of launch personality and visual confidence, translated into a neutral, copper-led Codex language.

## Typography

- **Display/Hero:** Native Apple/system display face — large, tight, and quiet enough for the imagery to carry atmosphere.
- **Body:** Native system sans for fast scanning and platform fidelity.
- **UI/Labels:** Native system sans with compact uppercase labels.
- **Data/Tables:** Native system sans with `font-variant-numeric: tabular-nums` when values need comparison.
- **Code:** `ui-monospace`, `SF Mono`, Menlo, monospace.
- **Loading:** No remote font dependency for the first surface; use platform fonts.
- **Scale:** 11/12px utility labels, 13/14px body UI, 17/20px lead, 32–56px section titles, 52–96px hero display.

## Color

- **Approach:** Restrained and material-led.
- **Primary accent:** `#B85B27` ember copper for focus, action, and ownership.
- **Strong accent:** `#8E421B` for light-theme text where contrast matters.
- **Light canvas:** `#F7F6F1` with `#FFFFFF` as the raised surface.
- **Dark canvas:** `#0B0C0C` carbon black with `#141615` as the raised surface.
- **Ink:** `#171512` in light mode and `#F2F0E9` in dark mode.
- **Semantic:** success `#3F795B` / `#9DD5AE`; warning uses copper; error stays a clear warm red; info uses neutral lilac only when needed.
- **Dark mode:** Redesign surfaces instead of inverting them. Lower saturation, preserve contrast, and never introduce navy as a substitute for black.

## Spacing

- **Base unit:** 4px.
- **Density:** Comfortable for the landing surface; compact-but-readable for the future operator surface.
- **Scale:** 4, 8, 12, 16, 24, 32, 48, 64, 96, 128px.

## Layout

- **Approach:** Hybrid. Full-canvas visual storytelling for the landing page; disciplined workspace layout for the app.
- **Grid:** One-column mobile; two-column hero and inspector layouts from 860px upward.
- **Max content width:** 1180px for editorial/marketing surfaces.
- **Border radius:** 10px marks, 14–16px controls, 22–28px image surfaces, pill only for compact toggles and actions.
- **App composition:** Primary workspace first, a narrow state rail second, and account/remote context available without becoming a card mosaic.

## Motion

- **Approach:** Intentional. Motion should signal presence, state changes, and handoff.
- **Entrance:** Orbital mark and visual layers settle into place once per session.
- **State transition:** Seat switching uses a clear pending → active → verified sequence rather than an instant color flip.
- **Hover/reveal:** Small lift and accent reveal on actionable surfaces; no perpetual motion in routine controls.
- **Reduced motion:** Disable looping animation and shorten transitions when `prefers-reduced-motion` is enabled.

## Product Rules

- Remote states are distinct: connected, waiting, failed, and unverified.
- Seats are isolated profiles with explicit active identity and rollback-safe switching.
- Claims about connection, login, or remote health must be backed by observable runtime evidence.
- Blue and navy are not part of the Codex-owned chrome palette.

## Decisions Log

| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-08-19 | White light / carbon-black night | Establishes a visible material contrast and removes the inherited blue/navy cast. |
| 2026-08-19 | Ember copper as the primary accent | Gives the companion its own identity without competing with runtime semantics. |
| 2026-08-19 | System fonts and local imagery | Keeps the surface fast, native, and resilient when disconnected. |
| 2026-08-19 | State-first product language | Remote and account tooling needs trust before spectacle. |
