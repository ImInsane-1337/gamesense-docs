# string.gmatch

Using [lua patterns](https://www.lua.org/pil/20.2.html), returns an iterator which will return either one value if no capture groups are defined, or any capture group matches.

```typescript
string.gmatch(str: string, pattern: string): function
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| str | String to search. | string |
| pattern | Pattern to search for. | string |

Returns `iterator: function`
