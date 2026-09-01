# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Solo tool for its author: a technical practitioner who writes estimates for
technical proposals. Working situation is drafting a proposal and needing a
defensible hours breakdown. Not shared with teammates or clients as a product;
its output (Markdown) is what other people see.

## Product Purpose

Turn the natural way of estimating — list high-level work, break each item into
progressively finer bullets, then attach hours only at the finest level — into a
live document where those leaf hours roll up to every parent automatically. It
exists to remove the onerous, error-prone manual summing that the author
otherwise does by hand. Success is producing a correct, well-structured hours
breakdown fast, then dropping it straight into the proposal.

## Positioning

Hours are entered only on leaf bullets and parents are always computed, never
typed, so totals cannot silently drift from their parts. The estimate's storage
and interchange format is the same Markdown bullet list that goes into the
proposal itself — a lossless import/export round-trip — so there is no separate
spreadsheet or export step to reconcile.

## Operating Context

Used while authoring a technical proposal. The author outlines top-down, refines
into 2–3 (up to 5) levels of nesting, enters integer hours on the deepest
bullets, then copies the result as Markdown and pastes it into the proposal
document. Runs entirely in the browser, offline, with work persisted locally
between sessions.

## Capabilities and Constraints

- Keyboard-driven outliner: Enter creates a sibling (splitting text at the
  caret), Tab / Shift+Tab indent and outdent whole subtrees, Backspace removes
  an empty bullet, Arrow keys move between rows.
- Up to 5 levels of nesting.
- Integer hours only, editable only on leaf bullets; parents display a
  read-only computed sum and a live grand total is shown in the header.
- Collapsible parents (expanded by default; collapse state persists).
- Persistence to `localStorage`.
- Markdown import and copy-as-Markdown, with hours rendered as bold `**Nh**`
  and 2-space indentation.
- Dark mode with system-theme auto-detection and a manual toggle.
- Durable constraint: a single self-contained, offline HTML file — no backend,
  no build step, `localStorage` only.

## Scope Boundaries

Confirmed to stay a pure hours breakdown and roll-up tool. Explicitly out of
scope for now: monetary rates or dollar amounts, managing multiple saved
estimates, and additional export formats (CSV, PDF, etc.). Future work must not
add these without a new decision.

## Evidence on Hand

The only bundled content is a sample estimate embedded as "Load sample"
(a WikiWatershed / LibreChat / MMW MCP proposal breakdown) used to demonstrate
structure. There are no real customers, testimonials, benchmarks, pricing, or
external assets; future work must not fabricate any.

## Product Principles

- Parents are computed, never entered: totals always equal the sum of their
  leaves.
- Markdown is the source of truth and the interchange format; the tool must
  round-trip it losslessly.
- Offline-first and self-contained: one HTML file the author owns, no backend.
- Estimating is keyboard-first and fluid; structure should be as fast to write
  as a plain bullet list.
- Stay focused on hours breakdown; resist scope growth into pricing, multi-doc
  management, or export sprawl.
