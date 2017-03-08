# Emote

|Endpoint|
|---|
|https://api.xivdb.com/emote/[id]|
|https://api.xivdb.com/emote|

## content

> /emote/[id]

Get information about the emote: `[id]`.

eg: https://api.xivdb.com/emote/137

## list

> /emote

Get a list of all emotes

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/emote?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/emote?columns=id,name,icon

