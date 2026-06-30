# config

## Description

Configuration related lua functions

## Functions

### export
[config.export(): string](config/export.md)
> Returns the current config in the export format

### import
[config.import(config: string)](config/import.md)
> Imports a config in the export format

### load
[config.load(name: string, tab_name: string, container_name: string)](config/load.md)
> Loads an existing config.
> To load the specified config: config.load('Config name here')
> To load a tab from the specified config: config.load('Config name here', 'Tab name here')
> To load a container from the specified config: config.load('Config name here', 'Tab name here', 'Container name here')
