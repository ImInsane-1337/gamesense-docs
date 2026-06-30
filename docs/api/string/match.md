# string.match

Using [lua patterns](https://www.lua.org/pil/20.2.html), returns the first match of the pattern in the string `str`. If no match is found, it returns `nil`.

```typescript
string.match(str: string, pattern: string, start): table
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| str | String to search. | string |
| pattern | Pattern to search for. | string |
| start | Where to start the search. Defaults to 1, can be negative. | unknown |

Returns `captures: table`
