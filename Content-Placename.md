# Placename

|Endpoint|
|---|
|https://api.xivdb.com/placename/[id]|
|https://api.xivdb.com/placename|

Square-Enix terminology of placenames are the main areas that contain map. "Zones" are sections of a map and "Regions" are the regions!

## content

> /placename/[id]

Get information about the placename: `[id]`.

eg: https://api.xivdb.com/placename/125

## list

> /placename

Get a list of all placenames

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/placename?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/placename?columns=id,name,icon

