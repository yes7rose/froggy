# froggy
[![Build Status](https://travis-ci.org/kvark/froggy.svg?branch=master)](https://travis-ci.org/kvark/froggy)
[![Docs](https://docs.rs/froggy/badge.svg)](https://docs.rs/froggy)
[![Crates.io](https://img.shields.io/crates/v/froggy.svg)](https://crates.io/crates/froggy)
[![Gitter](https://badges.gitter.im/kvark/froggy.svg)](https://gitter.im/almost-ecs/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

Froggy is a prototype for [Component Graph System](https://github.com/kvark/froggy/wiki/Component-Graph-System). Froggy is not an ECS (it could as well be named "finecs" but then it would have "ecs" in the name... yikes)! Give it a try if:
  - you are open to new paradigms and programming models
  - you are tired of being forced to think in terms of ECS
  - you like simple composable things

Check [ecs_bench](https://github.com/lschmierer/ecs_bench) for performance comparisons with actual ECS systems.

## Example

```rust
extern crate froggy;

fn main() {
    let mut positions = froggy::Storage::new();
    // create entities
    let entities = vec![
        positions.create(1u8), positions.create(4u8), positions.create(9u8)
    ];
    // update positions
    for e in &entities {
        positions[e] += 1;
    }
}
```
## License

Licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in the work by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
