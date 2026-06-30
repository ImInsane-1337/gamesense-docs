# load

Loads a chunk of Lua source code from a string or a "reader" function.

If there are no syntactic errors, returns the compiled chunk as a function; otherwise, returns `nil` plus the error message.

If chunk is a function, load calls it repeatedly to get the chunk pieces. Each call to chunk must return a string that concatenates with previous results. A return of an empty string, nil, or no value signals the end of the chunk.

```typescript
load(chunk: string, chunkname: string, mode: string, env: table): function, string
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| chunk | The chunk of Lua source code to load. | string |
| chunkname | The name to associate with the chunk, used for error messages and debug information. When absent, it defaults to `chunk`, if chunk is a string, or to "=(load)" otherwise. | string |
| mode | Controls whether the chunk can be text or binary (that is, a precompiled chunk). It may be the string `"b"` (only binary chunks), `"t"` (only text chunks), or `"bt"` (both binary and text). The default is `"bt"`. | string |
| env | The environment to use for the chunk. Defaults to the current environment. | table |

Returns `function, error: string`
