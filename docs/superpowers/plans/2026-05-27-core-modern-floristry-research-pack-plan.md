# Core Modern Floristry Research Pack Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a sourced text research pack for filling future Flowers Cards across the core flowers of modern floristry.

**Architecture:** Create a Markdown research document plus a source log. Fully research the first five flowers first, then list the remaining core flowers as structured queue entries for later expansion.

**Tech Stack:** Markdown, web research, Git.

---

## File Structure

- Create: `research/core-modern-floristry-flowers.md`
  - Main research pack for card content.
- Modify/Create: `research/source-log.md`
  - Source tracking for factual claims, cultivar/type references, and useful indexes.
- Reference: `docs/superpowers/specs/2026-05-27-core-modern-floristry-research-pack-design.md`
  - Approved design and scope.

---

### Task 1: Create Research Pack Skeleton

**Files:**
- Create: `research/core-modern-floristry-flowers.md`
- Modify/Create: `research/source-log.md`

- [ ] **Step 1: Create main document with exact structure**

Create `research/core-modern-floristry-flowers.md` with:

```markdown
# Core Modern Floristry Flowers

Date: 2026-05-27

## Purpose

This document collects practical, sourced information for filling future Flowers Cards. It supports the product direction: a practical floristry workbook disguised as a beautiful visual atlas.

## How To Use This Document

Each completed flower entry should answer:

- what the flower is;
- when it is practically available;
- how a florist evaluates freshness;
- how it should be processed and stored;
- how it behaves in composition;
- which three varieties, types, or market groups are most useful for beginners;
- where to look up all other varieties.

## Entry Template

### Flower Name

**Names:** RU / EN / Latin

**Seasonality:** practical season and import notes.

**Composition Role:** focal, mass, line, texture, air, filler, greenery, accent.

**Character:** visual and emotional effect.

**Freshness Checks:**

- check 1;
- check 2;
- check 3.

**Processing After Purchase:**

- step 1;
- step 2;
- step 3.

**Storage And Vase Life:** temperature, water, vase life, sensitivity notes.

**Beginner Mistakes:**

- mistake 1;
- mistake 2.

**Three Useful Varieties / Types / Groups:**

1. Name — why it matters.
2. Name — why it matters.
3. Name — why it matters.

**All Other Varieties:** link and note.

**Card-Ready Notes:**

- poster card:
- story card:
- care card:
- varieties card:

**Sources:** links and notes.

---

## Fully Researched First Batch

Entries to complete first:

1. Rose
2. Peony
3. Moluccella
4. Hydrangea
5. Ranunculus

## Research Queue

### Spring Flowers

- Tulip
- Anemone
- Narcissus
- Hyacinth
- Lilac
- Muscari
- Fritillaria

### Year-Round Commercial Base

- Lisianthus
- Chrysanthemum
- Carnation
- Alstroemeria
- Gerbera
- Lily
- Calla

### Summer / Garden Cut Flowers

- Dahlia
- Cosmos
- Scabiosa
- Delphinium
- Matthiola
- Sweet Pea
- Astilbe

### Texture / Shape / Accent Flowers

- Amaranthus
- Celosia
- Craspedia
- Eryngium
- Protea
- Orchid

### Fillers And Greenery

- Gypsophila
- Statice / Limonium
- Waxflower
- Eucalyptus
- Ruscus
- Asparagus Fern
- Salal
```

- [ ] **Step 2: Create or extend source log**

Ensure `research/source-log.md` contains:

```markdown
# Source Log

Date: 2026-05-27

| Topic | Source | URL | Type | Trust Level | Used For | Notes |
| --- | --- | --- | --- | --- | --- | --- |
```

If the file already exists, preserve existing rows and update the date section only if it does not remove older notes.

- [ ] **Step 3: Verify skeleton**

Run:

```bash
test -f research/core-modern-floristry-flowers.md
test -f research/source-log.md
rg -n "Rose|Peony|Moluccella|Hydrangea|Ranunculus" research/core-modern-floristry-flowers.md
```

Expected: both files exist, and all five first-batch flower names are present.

- [ ] **Step 4: Commit**

Run:

```bash
git add research/core-modern-floristry-flowers.md research/source-log.md
git commit -m "Create core floristry research pack skeleton"
```

---

### Task 2: Research First Five Flowers

**Files:**
- Modify: `research/core-modern-floristry-flowers.md`
- Modify: `research/source-log.md`

- [ ] **Step 1: Gather sources**

For each first-batch flower, gather at least:

- one botanical identity source;
- one florist/grower handling or postharvest source;
- one cultivar/type/index source.

Use reliable sources such as:

- RHS;
- Kew Plants of the World Online;
- Missouri Botanical Garden;
- NC State Extension;
- university extension resources;
- grower or breeder catalogs;
- Wikipedia/Wikimedia only as variety index or orientation, not sole authority for handling.

- [ ] **Step 2: Fill Rose entry**

Complete the rose entry with:

- names;
- seasonality;
- composition role;
- character;
- freshness checks;
- processing;
- storage and vase life;
- beginner mistakes;
- three useful groups;
- all other varieties link;
- card-ready notes;
- sources.

Rose variety/group model:

1. Hybrid tea / large-headed commercial rose.
2. Spray rose.
3. Garden / English / garden-style rose.

Use "all other varieties" link to a broad rose cultivar or garden rose reference.

- [ ] **Step 3: Fill Peony entry**

Peony variety/group model:

1. Herbaceous peony.
2. Tree peony.
3. Itoh / intersectional peony.

Include cut-stage guidance because peony harvest stage strongly affects opening and vase life.

- [ ] **Step 4: Fill Moluccella entry**

Moluccella variety/group model:

1. Moluccella laevis / bells of Ireland.
2. Green bell spike market form.
3. Dried/fresh structural use as a practical floristry group.

If named cultivars are limited, explicitly say the floristry distinction is more about maturity, stem length, and fresh/dried use than cultivar diversity.

- [ ] **Step 5: Fill Hydrangea entry**

Hydrangea type model:

1. Hydrangea macrophylla.
2. Hydrangea paniculata.
3. Hydrangea arborescens.

Include "all other types" link covering quercifolia, serrata, and other hydrangeas.

- [ ] **Step 6: Fill Ranunculus entry**

Ranunculus variety/group model:

1. Butterfly ranunculus.
2. Cloni / Italian ranunculus.
3. Tecolote or standard florist ranunculus.

If source quality varies, mark named commercial groups as market/grower categories and cite supplier/grower pages.

- [ ] **Step 7: Update source log**

Every used source gets a row in `research/source-log.md` with:

- topic;
- source;
- URL;
- type;
- trust level;
- used for;
- limitations.

- [ ] **Step 8: Verification scan**

Run:

```bash
rg -n "TODO|TBD|source needed|unsourced|verify later" research/core-modern-floristry-flowers.md research/source-log.md
```

Expected: no accidental unresolved markers. Any true uncertainty must be written as a precise note, not as a placeholder.

- [ ] **Step 9: Commit**

Run:

```bash
git add research/core-modern-floristry-flowers.md research/source-log.md
git commit -m "Research first core floristry flowers"
```

---

### Task 3: Card-Fill Extraction Pass

**Files:**
- Modify: `research/core-modern-floristry-flowers.md`

- [ ] **Step 1: Review card-ready notes**

For each completed first-batch flower, make sure `Card-Ready Notes` contains concise copy for:

- poster card;
- story card;
- care card;
- varieties card.

- [ ] **Step 2: Add consistency labels**

For each completed flower, add a short label set:

```markdown
**Card Labels:** season / role / care sensitivity / type complexity
```

Example:

```markdown
**Card Labels:** spring-summer / focal / medium-sensitive / high type complexity
```

- [ ] **Step 3: Verify first batch completeness**

Run:

```bash
rg -n "Card-Ready Notes|All Other Varieties|Three Useful" research/core-modern-floristry-flowers.md
```

Expected: each phrase appears at least five times, once per completed first-batch flower.

- [ ] **Step 4: Commit**

Run:

```bash
git add research/core-modern-floristry-flowers.md
git commit -m "Add card-ready notes for first flower batch"
```

---

### Self-Review

- Spec coverage: covers the approved approach 2, around 35 core flowers, first five deep entries, and the variety/index rule.
- Scope: focused on a text research pack, not UI implementation.
- Verification: source log plus placeholder scan plus first-batch completeness scan.
