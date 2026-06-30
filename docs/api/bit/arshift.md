# bit.arshift

Returns the bitwise arithmetic right-shift of its first argument by the number of bits given by the second argument.
Arithmetic right-shift treats the most-significant bit as a sign bit and replicates it. Only the lower 5 bits of the shift count are used (reduces to the range [0..31]).

```typescript
bit.arshift(x: number, n: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | Value | number |
| n | Number of bits to shift by | number |

Returns `number`
