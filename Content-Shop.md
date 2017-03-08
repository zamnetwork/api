# Shop (WIP)

This is not really supported anymore, because Shop stuff is crazy...

|Endpoint|
|---|
|https://api.xivdb.com/shop/[id]|
|https://api.xivdb.com/shop|

## content

> /shop/[id]

Get information about the shop: `[id]`.

## list

> /shop

Get a list of all shops

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/shop?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/shop?columns=id,name,icon

