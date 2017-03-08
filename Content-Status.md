# Status

|Endpoint|
|---|
|https://api.xivdb.com/status/[id]|
|https://api.xivdb.com/status|

## content

> /status/[id]

Get information about the status: `[id]`.

eg: https://api.xivdb.com/status/1145

## list

> /status

Get a list of all statuss

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/status?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/status?columns=id,name,icon

