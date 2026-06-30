# bit.tohex

Converts its first argument to a hex string. The number of hex digits is given by the absolute value of the optional second argument. Positive numbers between 1 and 8 generate lowercase hex digits. Negative numbers generate uppercase hex digits. Only the least-significant 4*|n| bits are used. The default is to generate 8 lowercase hex digits.

```typescript
bit.tohex(x: number, n: number): string
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| x | Value to convert | number |
| n | Amount of hex digits to return | number |

Returns `string`
