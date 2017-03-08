# Mount

|Endpoint|
|---|
|https://api.xivdb.com/mount/[id]|
|https://api.xivdb.com/mount|

## content

> /mount/[id]

Get information about the mount: `[id]`.

eg: https://api.xivdb.com/mount/56

## list

> /mount

Get a list of all mounts

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/mount?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/mount?columns=id,name,icon

