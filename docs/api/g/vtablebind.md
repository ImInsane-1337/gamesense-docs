# vtable_bind

Utility for calling virtual functions on FFI objects. This variant works with Interfaces and doesn't require passing the this-pointer as the first argument every time.

```typescript
vtable_bind(module_name: string, interface_name: string, index: number, typestring: string, ...): function
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| module_name | Filename of the module that contains the interface | string |
| interface_name | Name of the interface | string |
| index | Index of the virtual function | number |
| typestring | A FFI type string, such as `"int(__thiscall*)(void*, int)"` | string |
| args | Additional arguments for the type (for use with [parameterized types](https://luajit.org/ext_ffi_semantics.html#:~:text=could%20possibly%20provide.-,Parameterized,-Types)) | unknown |

Returns `function`
