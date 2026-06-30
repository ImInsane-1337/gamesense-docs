# math.random

Returns a random number between the values provided.
When called without arguments, returns a uniform pseudo-random real number in the range [0,1]. When called with an integer number m, math.random returns a uniform pseudo-random integer in the range [1, m]. When called with two integer numbers m and n, math.random returns a uniform pseudo-random integer in the range [m, n].

LuaJIT uses a Tausworthe PRNG with period 2^223 to implement [math.random](random.md) and [math.randomseed(#randomseed).

When called without arguments it generates 52 pseudo-random bits for every call. The result is uniformly distributed between `0.0` and `1.0`. It's correctly scaled up and rounded for `math.random(n [,m])` to preserve uniformity.

Important: Neither this nor any other PRNG based on the simplistic math.random API is suitable for cryptographic use.

```typescript
math.random(min: number, max: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| min | Minimum value (inclusive). Defaults to 0. | number |
| max | Maximum value (inclusive). Defaults to 1. | number |

Returns `number`
