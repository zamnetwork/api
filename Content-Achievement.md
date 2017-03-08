# Achievements

|Endpoint|
|---|
|https://api.xivdb.com/achievement/[id]|
|https://api.xivdb.com/achievement|

## content

> /achievement/[id]

Get information about the achievement: `[id]`.

## list

> /achievement

Get a list of all achievements

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/achievement?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/achievement?columns=id,name,icon

