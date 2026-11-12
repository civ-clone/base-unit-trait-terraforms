# base-unit-trait-terraforms

The `Terraforms` unit trait: a unit type with it can work the land.

A unit type with this trait can do terrain work: irrigate, mine, build roads and railroads, clear or plant, clean pollution, and be automated to do so.

For example: Civ1: Settlers. Civ2: Settlers and Engineers.

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(Terraforms)`:

```ts
import Terraforms from '@civ-clone/base-unit-trait-terraforms/Terraforms';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, Terraforms));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
