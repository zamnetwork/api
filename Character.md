# Character

|Endpoint|
|---|
|https://api.xivdb.com/character/[id]|
|https://api.xivdb.com/character|

**Note on language parameter**
Currently XIVDB parses the English version of Lodestone and stores some of the data in plain text. This includes: Titles, grand company names, races, gender. This will be English only. I am working on moving this to object state so it can be multiple languages.

---

## content

> /character/[id]

Get information about the character: `[id]`.

---

## list

There is no list feature for characters, this is due to the high volume of characters in the same.

---

## parameters

> `data=events`

Get characters timeline events

eg: https://api.xivdb.com/character/730968?data=events

---

> `data=tracking`

Get characters timeline tracking events, these are things such as name changes, race changes, server changes, etc.

- eg: https://api.xivdb.com/character/730968?data=tracking

---

> `data=gearsets`

Get all recorded gearsets on the character. XIVDB saves gearsets for each class.

- eg: https://api.xivdb.com/character/730968?data=gearsets

---

> `data=achievements`

Get all achievements for a character

- eg: https://api.xivdb.com/character/730968?data=achievements

---

> `data=achievements_possible`

Get a list of achievements ID that this character can possible get. As of March 2017 this is currently a list of all achievements excluding/including Legacy achievements based on the characters creation date. 

- eg: https://api.xivdb.com/character/730968?data=achievements_possible

|**Note regarding restricted achievements**|
|---|
|Some achievements are exclusive, for example a character can only get the "Leaving [nation]" achievement for the town nation they joined when the character was created. For 1.0 characters they can have 2 of the 3 nation achievements (as players could change nation in 2.0 release). Characters created after 2.0 can only get 1 of the 3 achievements. Lodestone will always show all 3 achievements as possible to obtain.

You would need to handle this manually in your application as XIVDB currently does not do anything about it (will do at some point). If SE ever fix their achievements pages, the route will automatically reflect the correct achievements.|

---

> `data=achievements_obtained`

Get a list of achievement ID that this character has obtained. This is useful if you want a very lightweight list of obtained achievements and their obtained date

- eg: http://api.xivdb.com/character/730968?data=achievements_obtained

