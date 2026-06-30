# string.gsub

Using [lua patterns](https://www.lua.org/pil/20.2.html), returns a copy of `str` with all matches of the pattern replaced by the given replacement string.

The pattern may be a string, a table or a function.

- If it is a string, then it can contain captures.
- If it is a table, the match is looked up in the table as a key, and the value (string) is used to replace it, if it exists.
- If it is a function, then the function is called for each match, with the value of the match as the first argument, the value of the n argument as the second argument, and the position of the match as the third argument.
The function must then return the replacement string to be used for the match.

```typescript
string.gsub(str: string, pattern: string, replacement: string, max: number): string, number
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| str | String to search. | string |
| pattern | Pattern to search for. | string |
| replacement | Replacement string or function. | string |
| max | Maximum number of replacements. | number |

Returns `string, number`
