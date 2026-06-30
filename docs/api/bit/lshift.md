# bit.lshift

Returns the bitwise logical left-shift of its first argument by the number of bits given by the second argument. Logical shifts treat the first argument as an unsigned number and shift in 0-bits. Only the lower 5 bits of the shift count are used (reduces to the range [0..31]).

```typescript
bit.lshift(x: number, n: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | Value | number |
| n | Number of bits to shift by | number |

Returns `number`
