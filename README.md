# Proposal Ledger

A single-file, offline web app for building **hours estimates for technical
proposals**. Write your work as a nested outline, put hours on the deepest
bullets, and every parent total is summed automatically. Copy the result as
Markdown straight into your proposal.

Open [index.html](index.html) in any modern browser — that's the whole app. No
build step, no server, no dependencies.

---

## Why it exists

Estimating a proposal usually means listing high-level work, breaking each item
into finer and finer bullets, and adding hours once the detail is fine enough —
then summing those hours back up to every parent by hand. That manual roll-up is
tedious and error-prone. Proposal Ledger does the summing for you: **you only
ever type numbers on leaf bullets, and parents are always computed.**

## Core model

- The estimate is an **outline** of bullets, up to **5 levels** deep.
- A **leaf** (a bullet with no children) has an **editable, integer** hour value.
- A **parent** (a bullet with children) shows a **read-only computed total** =
  the sum of all its descendant leaves.
- The header shows a **live grand total** of every leaf.

## Using it

### Keyboard (the fast way)

| Key | Action |
| --- | --- |
| `Enter` | New bullet below (splits text at the cursor) |
| `Tab` | Indent the bullet (and its children) one level |
| `Shift` + `Tab` | Outdent one level |
| `Backspace` (empty bullet) | Delete the bullet |
| `↑` / `↓` | Move the caret between rows |

Type in a leaf's number box to set its hours. Focusing a box that reads `0`
clears it so you can just type; leaving it empty resets it to `0`. Hours are
integers only.

### Mouse

Hover a row to reveal a floating toolbar: **indent**, **outdent**, **move up**,
**move down**, and **delete**. Click the **chevron** on a parent to collapse or
expand its children (collapsed parents still show their total).

### Toolbar

- **Copy Markdown** — copies the whole outline to your clipboard as Markdown.
- **Import Markdown…** — paste a nested bullet list to replace the current one.
- **Load sample** — loads a demonstration estimate.
- **Theme toggle** (`☾ / ☀`) — switch light/dark; auto-detects your system theme.
- **Clear all** — start over.

## Markdown format

Hours are written as a bold, unit-suffixed value at the end of each line, and
nesting uses **2 spaces per level**:

```markdown
* Meetings **20h**
  * Kickoff **2h**
  * Sprintly Meetings **10h**
  * Ad Hoc Pairing Sessions **8h**
* Feature 1 **20h**
  * Task 1 **4h**
  * Task 2 **8h**
    * Subtask 1 **4h**
    * Subtask 2 **4h**
```

- **Export** (Copy Markdown) writes a total on **every** row, including parents.
- **Import** accepts `**8h**` or `**8**`. Hours are applied to **leaf** bullets;
  parent totals are always **recomputed** from the leaves, so the numbers you see
  are guaranteed to add up. `*`, `-`, and `+` bullets are all accepted.

## Persistence

Everything is saved to your browser's `localStorage` on every change and
restored when you reopen the file — including the outline, hours, collapsed
state, and your theme choice. Nothing leaves your machine.

## Constraints (by design)

- **Single self-contained offline HTML file** — no backend, no build, no network.
- **Integer hours** only.
- Scope is intentionally limited to an hours breakdown and roll-up; it does not
  do rates/dollars, multiple saved estimates, or other export formats.

## Design

The visual system (the "Proposal Ledger" — serif outline, monospace ledger
column, one rationed blue accent) is documented in [DESIGN.md](DESIGN.md), with
machine-readable tokens and component snippets in
[.impeccable/design.json](.impeccable/design.json). Product context lives in
[PRODUCT.md](PRODUCT.md).
