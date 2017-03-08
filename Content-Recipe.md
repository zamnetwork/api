# Recipe

|Endpoint|
|---|
|https://api.xivdb.com/recipe/[id]|
|https://api.xivdb.com/recipe|

## content

> /recipe/[id]

Get information about the recipe: `[id]`.

eg: https://api.xivdb.com/recipe/32225

## list

> /recipe

Get a list of all recipes

> Parameter: `schema=XXX`

The schema can be adjusted for lists, eg:

- https://api.xivdb.com/recipe?schema=1

This will list all fields that can be selected using the `columns` option

> Parameter: `columns=xxx,yyy,zzz`

eg: 

- https://api.xivdb.com/recipe?columns=id,name,icon

