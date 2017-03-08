# Gathering

|Endpoint|
|---|
|https://api.xivdb.com/gathering/[id]|
|https://api.xivdb.com/gathering|

## content

> /gathering/[id]

Get information about the gathering: `[id]`.

eg: https://api.xivdb.com/gathering/300000355

## list

> /gathering

Get a list of all gatherings

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/gathering?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/gathering?columns=id,name,icon

