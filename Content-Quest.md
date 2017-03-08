# Quest

|Endpoint|
|---|
|https://api.xivdb.com/quest/[id]|
|https://api.xivdb.com/quest|

## content

> /quest/[id]

Get information about the quest: `[id]`.

eg: https://api.xivdb.com/quest/67912

## list

> /quest

Get a list of all quests

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/quest?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/quest?columns=id,name,icon

