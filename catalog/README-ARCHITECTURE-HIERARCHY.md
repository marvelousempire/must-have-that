# Must-Have That — hierarchical catalog and breadcrumb law

**Owning product:** Must-Have That (TS-CORE-073). This **extends** the existing `registry/must-haves.json`; it does not create a second status registry.

## Drill-down (general left → specific right)

```text
Must Haves → Architecture → Automata → Global / Page
                                         └→ Page → Concept → Section → Container
                                                         → Feature → Module → Row → Element
```

The user's named levels **Concept, Container, Feature, Module, Element** are preserved. Section and Row remain first-class physical placement levels because the existing Father shell atlas already has **section_id, container_id, row_id, element_id**. An actual page can omit unused intermediate levels but must never lose the stable semantic IDs. The path is a scoped breadcrumb, **not** an assertion that every feature is visually inside a module or that every concept maps to a unique DOM element.

## Contract

- The left side is an inherited requirement taxonomy. The right side is an increasingly specific target scope; global Automata requirements apply to all its pages.
- Every requirement resolves to a canonical Must-Have That ID; do not clone requirements at each depth. Record an explicit `applies_to` or scope path.
- Keep **category**, **product**, **page**, **concept**, **section**, **container**, **feature**, **module**, **row**, and **element** separately addressable and navigable.
- Each row carries original wording, intent, owner, CCK identity/version, implementation state, approved visibility, test, receipt, supersession and source revision.
- Use distinct statuses **requested → cck-pending → contracted → implemented → source-tested → runtime-witnessed → commissioned**. The new Automata rows are **not** cleared merely because entered.
- When a parent requirement changes, compute the affected children, preserve exceptions only with approval, and verify the relevant subtree.
- Presentation must support breadcrumb navigation, hierarchical tree, filtered matrix, per-node detail and traceability to owner sources.
- Requirement **visibility** is not UI visibility: publishing an element is an explicit, server-authorized control, never inherited from being present in the catalog.

## Owning references

- [Structured Automata catalog seed](2026-10-11-automata-architecture-hierarchy.json)
- [Existing canonical must-haves](../registry/must-haves.json)
- [Father shell placement identifiers](https://github.com/marvelousempire/nephew/blob/main/plans/0589-briefcase-shell-atlas-zone-ids.md)
- [CCK-first gate](https://github.com/marvelousempire/that-app-studio/blob/main/docs/CCK-FIRST-ASSEMBLY-FLOW.md)
- [Automata modularity contract](https://github.com/marvelousempire/automata/blob/main/docs/architecture/MANDATORY-MODULAR-PLATFORM-SEPARATION-2026-10-11.md)

**Construction gate:** Inventory/reconcile the owning CCKs first. The seed records requirements only; it neither commissions page controls nor verifies that every nesting level exists in Automata's current UI.
