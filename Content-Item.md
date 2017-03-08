# Item

|Endpoint|
|---|
|https://api.xivdb.com/item/[id]|
|https://api.xivdb.com/item|

## content

> /item/[id]

Get information about the item: `[id]`.

eg: https://api.xivdb.com/item/17433

## list

> /item

Get a list of all items

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/item?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/item?columns=id,name,icon

