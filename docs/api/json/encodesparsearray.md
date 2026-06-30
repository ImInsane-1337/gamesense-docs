# json.encode_sparse_array

[json.stringify](encodesparsearray.md) classifies a Lua table into one of three kinds when encoding a JSON array. This is determined by the number of values missing from the Lua array as follows:

Normal: All values are available.
Sparse: At least 1 value is missing.
Excessively sparse: The number of values missing exceeds the configured ratio.

It encodes sparse Lua arrays as JSON arrays using JSON `null` for the missing entries.
An array is excessively sparse when all the following conditions are met:
`ratio > 0`, `maximum_index > safe`, `maximum_index > item_count * ratio`

JSON will never consider an array to be excessively sparse when `ratio` = `0`. The `safe` limit ensures that small Lua arrays are always encoded as sparse arrays.
By default, attempting to encode an *excessively sparse* array will generate an error. If `convert` is set to true, excessively sparse arrays will be converted to a JSON object.

The current settings are always returned. A particular setting is only changed when the argument is provided (non-`nil`).

```typescript
json.encode_sparse_array()
```
