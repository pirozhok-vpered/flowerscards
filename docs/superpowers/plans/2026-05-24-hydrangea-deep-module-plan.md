# Hydrangea Deep Module Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a deeper pilot module for hydrangea that turns the atlas into a practical floristry workbook disguised as a visual botanical atlas.

**Architecture:** Keep the current static prototype, but add structured research files and expand only the hydrangea section first. The hydrangea module becomes the model for future flowers: poster, story, buying checks, processing/storage, and types/composition.

**Tech Stack:** Markdown research notes, static HTML, CSS.

---

### File Structure

- Modify: `briefs/creative-concept-summary.md`
  - Purpose: preserve the product concept and hydrangea pilot decision.
- Create: `research/hydrangea-deep-research.md`
  - Purpose: sourced research notes for hydrangea history, groups, buying checks, processing, storage, and composition.
- Create: `research/source-log.md`
  - Purpose: track every factual and photo source with URL, source type, trust level, and usage.
- Modify: `prototype/index.html`
  - Purpose: replace the current three-card hydrangea section with the deeper pilot sequence.
- Modify: `prototype/styles.css`
  - Purpose: add reusable styles for the deeper module cards.

---

### Task 1: Research Skeleton

**Files:**
- Create: `research/hydrangea-deep-research.md`
- Create: `research/source-log.md`

- [ ] **Step 1: Create hydrangea research document**

Add this exact structure to `research/hydrangea-deep-research.md`:

```markdown
# Hydrangea Deep Research

Date: 2026-05-24

## Purpose

Research hydrangea as the pilot flower for the deeper Flowers Cards learning module.

## Module Questions

### 1. Story / Character

- Where does hydrangea come from botanically and culturally?
- What is memorable about its name, symbolism, or use?
- What character does it bring to a composition?

### 2. Buy & Check

- What does a fresh hydrangea look like?
- What are signs of dehydration or poor storage?
- What stem, leaf, head, and petal checks matter at purchase?
- Which bloom stage is best for floristry?

### 3. Process & Store

- How should hydrangea be unpacked?
- What cut angle or stem treatment is recommended?
- How much water does it need?
- When should it be rehydrated or fully soaked?
- What storage temperature and humidity are recommended?
- What recovery techniques are credible and when should they be labeled as florist techniques?

### 4. Types & Varieties

- Which groups matter for a beginner florist?
- How do macrophylla, paniculata, arborescens, quercifolia, and serrata differ visually?
- Which types are most relevant in cut-flower work?
- Which differences change care, seasonality, or composition?

### 5. Compose

- What role does hydrangea play in arrangements?
- Which forms, textures, and colors pair well with it?
- When should a beginner avoid using it?

## Researched Notes

Write sourced notes here.

## Claims To Verify

List claims that need more than one source here.
```

- [ ] **Step 2: Create source log**

Add this exact structure to `research/source-log.md`:

```markdown
# Source Log

Date: 2026-05-24

| Topic | Source | URL | Type | Trust Level | Used For | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Hydrangea groups | RHS | https://www.rhs.org.uk/plants/hydrangea/pruning-guide | horticultural authority | high | group differences | Use for group distinction, not cut-flower handling. |
| Hydrangea species | NC State Extension | https://extensiongardener.ces.ncsu.edu/gardening-publications-2/extgardener-previous-newsletters/extgardener-past-features/extgardener-hydrangeas-hallmarks-of-the-southern-garden/ | extension | high | species/group overview | Use for macrophylla, paniculata, arborescens, quercifolia context. |
| Hydrangea cut care | OSU Extension | https://extension.oregonstate.edu/gardening/flowers-shrubs-trees/general-care-hydrangeas | extension | medium-high | recovery techniques | Label boiling water/alum as techniques to verify before final teaching copy. |
```

- [ ] **Step 3: Verify files exist**

Run:

```bash
test -f research/hydrangea-deep-research.md
test -f research/source-log.md
```

Expected: exit code 0 for both commands.

- [ ] **Step 4: Commit**

Run:

```bash
git add research/hydrangea-deep-research.md research/source-log.md
git commit -m "Add hydrangea deep research skeleton"
```

---

### Task 2: Sourced Hydrangea Research Pass

**Files:**
- Modify: `research/hydrangea-deep-research.md`
- Modify: `research/source-log.md`

- [ ] **Step 1: Research authoritative sources**

Use current, source-attributed references for:

- hydrangea groups and botanical distinctions;
- cut-flower hydration and vase life;
- florist handling and recovery techniques;
- composition uses and warnings.

- [ ] **Step 2: Record every source**

For each source used, add a row to `research/source-log.md` with:

- topic;
- source name;
- URL;
- source type;
- trust level;
- what the atlas uses it for;
- limitations.

- [ ] **Step 3: Write practical notes**

Fill `research/hydrangea-deep-research.md` with concise notes under:

- Story / Character;
- Buy & Check;
- Process & Store;
- Types & Varieties;
- Compose;
- Claims To Verify.

- [ ] **Step 4: Verification scan**

Run:

```bash
rg -n "TODO|TBD|unsourced|verify later" research/hydrangea-deep-research.md research/source-log.md
```

Expected: no unresolved placeholder lines. If a claim still needs verification, keep it under `Claims To Verify` with the exact uncertainty.

- [ ] **Step 5: Commit**

Run:

```bash
git add research/hydrangea-deep-research.md research/source-log.md
git commit -m "Research hydrangea deep module"
```

---

### Task 3: Hydrangea Deep Prototype Cards

**Files:**
- Modify: `prototype/index.html`
- Modify: `prototype/styles.css`

- [ ] **Step 1: Expand hydrangea section to five cards**

In `prototype/index.html`, replace the hydrangea three-card set with:

1. Poster Card.
2. Story / Character Card.
3. Buy & Check Card.
4. Process & Store Card.
5. Types & Compose Card.

- [ ] **Step 2: Add card content from research**

Use only sourced or clearly provisional notes from `research/hydrangea-deep-research.md`.

Each card should be concise enough to remain readable:

- Buy & Check: 5-6 inspection points.
- Process & Store: 5-6 practical steps.
- Types & Compose: 4-5 groups plus composition guidance.

- [ ] **Step 3: Add reusable styles**

In `prototype/styles.css`, add styles for:

- `.deep-module`;
- `.practice-card`;
- `.practice-card__topline`;
- `.practice-card__head`;
- `.check-list`;
- `.type-strip`.

The styles should align with the existing poster/story/index card family.

- [ ] **Step 4: Manual browser verification**

Open:

```text
file:///Users/nikosi/Documents/Codex/hobby%20projects/flowerscards/prototype/index.html
```

Check:

- hydrangea module reads in the correct order;
- text does not overlap;
- cards share a visual system;
- notes are readable in the in-app browser.

- [ ] **Step 5: Commit**

Run:

```bash
git add prototype/index.html prototype/styles.css
git commit -m "Expand hydrangea into deep learning module"
```

---

### Task 4: Real Photo Test

**Files:**
- Create: `assets/photos/hydrangea/README.md`
- Modify: `prototype/index.html`
- Modify: `prototype/styles.css`
- Modify: `research/source-log.md`

- [ ] **Step 1: Select one free hydrangea photo**

Choose a free image that matches the art direction:

- isolated or clean hydrangea subject;
- enough negative space;
- not a busy bouquet;
- clear license;
- source and author recorded.

- [ ] **Step 2: Save photo source notes**

Create `assets/photos/hydrangea/README.md` with:

```markdown
# Hydrangea Photo Sources

| File | Source | Author | URL | License URL | Notes |
| --- | --- | --- | --- | --- | --- |
```

- [ ] **Step 3: Add source log entry**

Add the photo source to `research/source-log.md`.

- [ ] **Step 4: Place the image in the poster card**

Update the hydrangea Poster Card so the real image can be tested against the existing graphic style.

- [ ] **Step 5: Manual verification**

Open the prototype and check:

- photo placement does not obscure text;
- photo feels consistent with the art direction;
- poster still works without relying on the CSS flower.

- [ ] **Step 6: Commit**

Run:

```bash
git add assets/photos/hydrangea prototype/index.html prototype/styles.css research/source-log.md
git commit -m "Test real hydrangea photo in poster card"
```

---

### Self-Review

- Spec coverage: covers the confirmed direction of a practical floristry workbook disguised as a visual atlas, using hydrangea as the pilot.
- Scope: limited to hydrangea, so the work is focused enough for one implementation cycle.
- Known non-code verification: this is a static creative prototype, so verification is manual browser review plus source/placeholder scans.
