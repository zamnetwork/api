# FATE

|Endpoint|
|---|
|https://api.xivdb.com/fate/[id]|
|https://api.xivdb.com/fate|

## content

> /fate/[id]

Get information about the fate: `[id]`.

eg: https://api.xivdb.com/fate/624

## list

> /fate

Get a list of all fates

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/fate?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/fate?columns=id,name,icon

