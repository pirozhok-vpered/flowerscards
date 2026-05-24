# Flowers Cards Creative Concept Summary

Date: 2026-05-24

## Project

Flowers Cards is a visual learning atlas for a beginning florist. The goal is to make flower study feel like a designed product: beautiful, collectible, clear, and practical.

The current prototype lives at:

- `prototype/index.html`
- `prototype/styles.css`

## Current Creative Direction

The visual language is:

- archival botanical poster;
- modern editorial typography;
- muted seasonal color fields;
- one flower as the visual hero;
- grain, print texture, and poster-like microtype;
- practical florist knowledge presented as designed cards, not office tables.

The strongest current direction is the flower poster card. Future work should preserve that feeling while making the practical and historical cards equally intentional.

## Card Sequence

Each flower now uses a three-card sequence:

1. Poster Card
2. Story / Context Card
3. Care Card

This sequence should repeat per flower:

- Rose poster -> Rose story -> Rose care
- Tulip poster -> Tulip story -> Tulip care
- Hydrangea poster -> Hydrangea story -> Hydrangea care

The sequence is designed so the user first feels the flower visually, then understands its cultural/botanical context, then learns how to work with it as a florist.

## Card 1: Poster Card

Purpose:

- create desire and visual memory;
- show the flower as an object;
- establish seasonal mood and color;
- feel like something worth saving.

Content:

- common Russian name;
- Latin name;
- season or availability hint;
- 1-2 practical micro-notes;
- main flower visual.

Design:

- one dominant flower image or botanical silhouette;
- strong flat background color;
- large serif title;
- small functional typography around the edges;
- generous negative space;
- no unexplained codes such as A1/B3.

Future real-photo behavior:

- the photo should replace the current CSS flower inside the same visual slot;
- prefer isolated stems, single blooms, botanical silhouettes, or clean close-ups;
- avoid busy bouquet photos and generic stock scenes.

## Card 2: Story / Context Card

Purpose:

- add inspiration and memory;
- explain why the flower matters;
- bring history, geography, cultural associations, or unusual facts;
- keep the atlas from feeling like a dry manual.

Content:

- short historical or cultural note;
- one memorable fact;
- practical interpretation for floristry;
- small note about future variety/type structure.

Design:

- quieter than the poster card, but still editorial;
- large roman numeral or visual mark;
- serif text, not generic body copy;
- one small bottom note;
- same seasonal palette family as the poster.

Tone:

- poetic but useful;
- no long encyclopedia paragraphs;
- avoid fake certainty when history varies by source.

## Card 3: Care Card

Purpose:

- teach how to handle the flower in florist practice;
- show seasonality, vase life, cut, hydration, storage, and common mistakes;
- become the practical reference layer.

Current fields:

- Season;
- Vase life / стойкость;
- Cut angle / срез;
- Water / hydration;
- Ideal conditions;
- Varieties or types;
- Beginner mistake or special behavior.

Design improvements already made:

- care card now follows the same card family as the poster;
- top microline matches the poster logic;
- large serif flower name and Latin name;
- data presented in a ruled editorial grid;
- beginner mistake moved to the bottom and reduced in scale.

Open creative issue:

- care cards should become more visually distinctive and less plain while staying readable.

Possible next experiments:

- use a small vertical seasonal bar;
- add a tiny care glyph system;
- turn care fields into modular blocks instead of a pure list;
- add one mini "type strip" for varieties;
- use color-coded care intensity.

## Variety / Type Logic

The atlas should not treat every flower as one generic object.

Recommended content hierarchy:

1. Species or market flower card: broad behavior and core handling.
2. Type group: important groups that change look, season, or care.
3. Variety notes: named cultivars, colors, source regions, and special handling.

This keeps beginner cards clear while allowing professional expansion.

## Hydrangea Example

Hydrangea should be structured by group/type before individual cultivar names.

Groups to track:

- Hydrangea macrophylla: classic bigleaf/mophead/lacecap florist reference.
- Hydrangea paniculata: cone-shaped panicle form; different visual role and seasonality.
- Hydrangea arborescens: smooth/tree-like hydrangea; Annabelle-type forms.
- Hydrangea quercifolia: oakleaf hydrangea; distinctive leaves and cone clusters.
- Hydrangea serrata: mountain hydrangea; often lacecap-like.

Working hypothesis:

- core cut-flower principles overlap: hydration, clean water, fresh cut, cool storage;
- visual role, seasonality, stem texture, head density, and expected vase behavior may differ by group and cultivar;
- the atlas should show this as "type-aware care", not a single generic instruction.

Existing note file:

- `research/hydrangea-structure-notes.md`

## Starter Flower Set

Current prototype:

- rose;
- tulip;
- hydrangea.

Planned basic assortment:

- rose;
- tulip;
- peony;
- hydrangea;
- ranunculus;
- chrysanthemum;
- lisianthus;
- alstroemeria;
- carnation;
- greenery and fillers.

## Photo Direction

First full visual pass should use free photo sources only, with strict art direction.

Photo rules:

- avoid random bouquet stock;
- prefer one flower, one stem, silhouette, or controlled close-up;
- consistent light temperature;
- enough negative space for poster typography;
- no fake cultivar precision from a generic image;
- record source, author, link, and license page.

## Known Design Preferences From Review

Keep:

- poster cards with strong botanical silhouettes;
- muted red/olive/cream palette direction;
- large serif flower names;
- archival poster mood;
- pair/sequence logic.

Fix or keep improving:

- all alignment should feel grid-based;
- microcopy must be meaningful, not decorative codes;
- care cards need more style and stronger relation to poster cards;
- practical text must be readable but not office-like;
- beginner mistake should stay small and low in the layout;
- real-photo test is needed next.

## Suggested Next Branch

Create a separate creative branch for refining the concept:

- branch name idea: `concept/card-system-v2`

Recommended next tasks:

1. Build one full polished flower sequence for hydrangea.
2. Test one real free photo in the poster slot.
3. Design the variety/type strip.
4. Improve the care card grid.
5. Add source tracking for factual and photo claims.
6. Decide whether the atlas should be horizontal A4, 16:9 slides, or both.

## Open Questions

- Should every flower get 3 cards, or only major flowers?
- Should varieties appear on the care card or as a fourth "variety map" card?
- Should real photos be cut out on flat backgrounds or placed as full images with masking?
- Should the final product feel more like a slide deck, printable cards, or an editorial PDF?
- How much practical detail belongs in the first visual layer versus expandable notes?
