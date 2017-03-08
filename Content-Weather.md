# Weather

|Endpoint|
|---|
|https://api.xivdb.com/weather/[id]|
|https://api.xivdb.com/weather|

## content

> /weather/[id]

Get information about the weather: `[id]`.

eg: https://api.xivdb.com/weather/51

## list

> /weather

Get a list of all weathers

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/weather?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/weather?columns=id,name,icon

