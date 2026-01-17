# Affinity Control: Disabled vs Performance

## Affinity Control Disabled
- OS manages thread scheduling
- Allows dynamic CPU scaling and migration

**Pros**
- Better thermal balance
- Often smoother sustained emulation on mobile devices
- Less risk of thermal throttling

**Cons**
- Slightly less deterministic thread behavior

## Affinity Control Performance
- Pins emulator threads to performance cores
- Reduces scheduling variance

**Pros**
- Higher peak performance
- More consistent short-term benchmarks

**Cons**
- Increased heat buildup
- Higher chance of sustained throttling

## Practical Guidance
- Long play sessions → Disabled
- Short benchmarking or bursts → Performance