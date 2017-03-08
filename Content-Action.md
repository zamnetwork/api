# Action

|Endpoint|
|---|
|https://api.xivdb.com/action/[id]|
|https://api.xivdb.com/action|

## content

> /action/[id]

Get information about the action: `[id]`.

eg: http://api.xivdb.com/action/3559/the+wanderer's+minuet

## list

> /action

Get a list of all actions

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/action?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/action?columns=id,name,icon

