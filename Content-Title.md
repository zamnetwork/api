# Title

|Endpoint|
|---|
|https://api.xivdb.com/title/[id]|
|https://api.xivdb.com/title|

## content

> /title/[id]

Get information about the title: `[id]`.

eg: https://api.xivdb.com/title/324

## list

> /title

Get a list of all titles

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/title?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/title?columns=id,name,icon

