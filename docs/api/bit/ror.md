# bit.ror

Returns the bitwise right rotation of its first argument by the number of bits given by the second argument. Bits shifted out on one side are shifted back in on the other side. Only the lower 5 bits of the rotate count are used (reduces to the range [0..31]).

```typescript
bit.ror(x: number, n: number): number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | Value | number |
| n | Number of bits to rotate by | number |

Returns `number`
