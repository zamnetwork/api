# NPC

|Endpoint|
|---|
|https://api.xivdb.com/npc/[id]|
|https://api.xivdb.com/npc|

## content

> /npc/[id]

Get information about the npc: `[id]`.

eg: https://api.xivdb.com/npc/1019613

## list

> /npc

Get a list of all npcs

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/npc?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/npc?columns=id,name,icon

