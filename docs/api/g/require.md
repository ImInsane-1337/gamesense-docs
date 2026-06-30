# require

Loads a Lua module. The `package.path` is searched for the module, and the first file found is loaded. If the module returns a value, that value is returned by require, otherwise `true` is returned.
Workshop libraries can be loaded using `require "gamesense/<id>"`, if you are subscribed to them.

```typescript
require(modname: string):
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| modname | The name of the module to load. | string |

Returns `module: undefined`
