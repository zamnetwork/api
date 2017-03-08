# Enemy

|Endpoint|
|---|
|https://api.xivdb.com/enemy/[id]|
|https://api.xivdb.com/enemy|

## content

> /enemy/[id]

Get information about the enemy: `[id]`.

eg: https://api.xivdb.com/enemy/5554

## list

> /enemy

Get a list of all enemys

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/enemy?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/enemy?columns=id,name,icon

