# string.find
info
More information on [lua patterns](https://www.lua.org/pil/20.2.html)

# string.find

Looks for the first match of the pattern in the string `str`. If it finds a match, then it returns the indices of `str` where the occurrence starts and ends; otherwise, it returns `nil`.

Passing true as the fourth argument turns off pattern matching facilities, so the function does a plain “find substring” operation, with no characters in the pattern being considered “magic”. Note that if `no_patterns` is given, then `start` must be given as well.

```typescript
string.find(str: string, pattern: string, start: number, no_patterns: boolean): number, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| str | String to search. | string |
| pattern | Pattern to search for. | string |
| start | Start index. Defaults to 1 | number |
| no_patterns | If true, then pattern matching is disabled. | boolean |

Returns `start: number, end: number`
