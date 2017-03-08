# Instance

|Endpoint|
|---|
|https://api.xivdb.com/instance/[id]|
|https://api.xivdb.com/instance|

## content

> /instance/[id]

Get information about the instance: `[id]`.

eg: https://api.xivdb.com/instance/7

## list

> /instance

Get a list of all instances

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/instance?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/instance?columns=id,name,icon

