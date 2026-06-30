# vtable_thunk

Utility for calling virtual functions on FFI objects. This variant takes the this-pointer as the first argument and grabs the virtual function from it when called.

```typescript
vtable_thunk(index: number, typestring: string, ...): function
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| index | Index of the virtual function | number |
| typestring | A FFI type string, such as `"int(__thiscall*)(void*, int)"` | string |
| args | Additional arguments for the type (for use with [parameterized types](https://luajit.org/ext_ffi_semantics.html#:~:text=could%20possibly%20provide.-,Parameterized,-Types)) | unknown |

Returns `function`
