# entity.get_all

Returns an array of entity indices matching the classname. Pass no arguments for all entities. Dormant entities are not returned.

```typescript
entity.get_all(classname: string): table
```

## Arguments

| Name | Description | Type |
| --- | --- | --- |
| classname | String that specifies the class name of entities that will be added to the list, for example `"CCSPlayer"`. | string |

Returns `entities: table`
