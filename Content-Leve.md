# Leve

|Endpoint|
|---|
|https://api.xivdb.com/leve/[id]|
|https://api.xivdb.com/leve|

## content

> /leve/[id]

Get information about the leve: `[id]`.

eg: https://api.xivdb.com/leve/1196

## list

> /leve

Get a list of all leves

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/leve?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/leve?columns=id,name,icon

