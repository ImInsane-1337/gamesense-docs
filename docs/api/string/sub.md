# string.sub

Returns a substring of `str` starting at `s` and ending at `e`. Use negative numbers to start from the end of the string.

```typescript
string.sub(str: string, s: number, e: number): string
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| str | String to get the substring of. | string |
| s | Where to start the substring, inclusive. Defaults to 1. | number |
| e | Where to end the substring. Defaults to -1 (end of the string). | number |

Returns `string`
