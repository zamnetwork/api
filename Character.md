# Character

|Endpoint|
|---|
|https://api.xivdb.com/character/[id]|
|https://api.xivdb.com/character|

## content

> /character/[id]

Get information about the character: `[id]`.

## list

There is no list feature for characters, this is due to the high volume of characters in the same.

## parameters

> `data=events`

Get characters timeline events

eg: https://api.xivdb.com/character/730968?data=events

> `data=tracking`

Get characters timeline tracking events, these are things such as name changes, race changes, server changes, etc.

eg: https://api.xivdb.com/character/730968?data=tracking

> `data=gearsets`

Get all recorded gearsets on the character. XIVDB saves gearsets for each class.

eg: https://api.xivdb.com/character/730968?data=gearsets

> `data=achievements`

Get all achievements for a character

eg: https://api.xivdb.com/character/730968?data=achievements

> `data=achievements_possible`

Get a list of achievements ID that this character can possible get

eg: https://api.xivdb.com/character/730968?data=achievements_possible



