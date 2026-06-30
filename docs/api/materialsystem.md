# materialsystem

## Description

Functions for interacting with the source engine [material system](https://developer.valvesoftware.com/wiki/Material).
Refer to [the material type](https://gamesense-docs.pages.dev/docs/api/types/material) for information on how to modify a material.

## Functions

### arms_material
[materialsystem.arms_material(): material](materialsystem/armsmaterial.md)
> Returns a reference to the arms material when 'Hands' is enabled

### chams_material
[materialsystem.chams_material(): material](materialsystem/chamsmaterial.md)
> Returns a reference to the player chams material

### find_material
[materialsystem.find_material(path: string, force_load: boolean): material](materialsystem/findmaterial.md)
> Returns a reference to the material

### find_materials
[materialsystem.find_materials(path: string): table](materialsystem/findmaterials.md)
> Returns a table of materials matching the specified path

### find_texture
[materialsystem.find_texture(path: string)](materialsystem/findtexture.md)
> Returns a pointer to a texture, can be used to override textures with [material:set_shader_param](https://gamesense-docs.pages.dev/docs/api/types/material#set_shader_param).

### get_model_materials
[materialsystem.get_model_materials(entindex: number): table](materialsystem/getmodelmaterials.md)
> Returns a table of materials used by the specified entity's model

### override_material
[materialsystem.override_material(material: material, material_new: material)](materialsystem/overridematerial.md)
> Overrides all of a material properties with another material.

### viewmodel_material
[materialsystem.viewmodel_material(): material](materialsystem/viewmodelmaterial.md)
> Returns a reference to the arms material when 'Weapon viewmodel' is enabled
