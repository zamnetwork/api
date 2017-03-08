# Minion

|Endpoint|
|---|
|https://api.xivdb.com/minion/[id]|
|https://api.xivdb.com/minion|

## content

> /minion/[id]

Get information about the minion: `[id]`.

eg: https://api.xivdb.com/minion/189

## list

> /minion

Get a list of all minions

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/minion?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/minion?columns=id,name,icon

