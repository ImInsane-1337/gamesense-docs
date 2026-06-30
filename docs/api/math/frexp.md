# math.frexp

Returns `m` and `e` such that `x = m2e`, `e` is an integer and the absolute value of `m` is in the range ((0.5, 1) (or zero when `x` is zero).
Used to split the number value into a normalized fraction and an exponent.
Two values are returned: the first is a multiplier in the range 1/2 (inclusive) to 1 (exclusive) and the second is an integer exponent. The result is such that `x = m*2^e`.

```typescript
math.frexp(x: number): number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | N/A | number |

Returns `number, number`
