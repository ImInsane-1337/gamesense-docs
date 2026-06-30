# database

## Description

Persistent storage that lets you store lua values (including tables) between script / cheat reloads.

## Functions

### flush
[database.flush()](database/flush.md)
> Flushes the database to disk. This is automatically called when the script is reloaded, but you can call it manually if you want to force a flush.

### read
[database.read(key_name: string):](database/read.md)
> Gets a value from the database

### write
[database.write(key_name: string, value)](database/write.md)
> Writes a value to the database. Avoid calling this often. For example, call read at script load, then call write during the 'shutdown' event
