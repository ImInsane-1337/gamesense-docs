# cvar

## Description

A table letting you get and set the value of cvars and invoke the callbacks of concommands.

```lua
-- localize the cvar objectlocal cl_fullupdate = cvar.cl_fullupdate-- invoke a callback to the command as if you entered the command in the consolecl_fullupdate:invoke_callback()
```

```lua
--localize the cvar objectlocal cl_downloadfilter = cvar.cl_downloadfilter-- print the current value of the cvarclient.log(cl_downloadfilter:get_string())-- set the cvars valuecl_downloadfilter:set_string("none")-- print it againclient.log(cl_downloadfilter:get_string()) -- "none"
```
info
The documentation for the `cvar` type is unfinished as it relies on types that aren't in the docs yet.

## Functions

### __index
[cvar.__index(name: string): cvar](index.md)
> Finds a cvar by name and returns a [cvar object](https://gamesense-docs.pages.dev/docs/api/types/cvar) for it, or nil if it doesn't exist or is blocked for security reasons.
