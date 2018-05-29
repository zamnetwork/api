|XIVDB API| |
|---|---|
| Endpoint | https://api.xivdb.com/ |
| Protocol| `https` and `http` supported. |
| Language| **JSON** |
| Methods | **GET** only |
| SDK | Soon.. |

---

## about

The XIVDB API allows you to access various different game content in a very structured format. The entire site runs on top of the API so it is heavily modular and integrates well with web technologies.

---

## documentation

### search
- [Search](Search.md)
    - [Search Order Fields](Search-Order.md)
- [Lore Finder](Tools-Lore-Finder.md)

### content
- [Achievement](Content-Achievement.md)
- [Action](Content-Action.md)
- [Emote](Content-Emote.md)
- [Enemy](Content-Enemy.md)
- [Fate](Content-Fate.md)
- [Gathering](Content-Gathering.md)
- [Instance](Content-Instance.md)
- [Item](Content-Item.md)
- [Leve](Content-Leve.md)
- [Minion](Content-Minion.md)
- [Mount](Content-Mount.md)
- [NPC](Content-NPC.md)
- [Placename](Content-Placename.md)
- [Quest](Content-Quest.md)
- [Recipe](Content-Recipe.md)
- [Shop](Content-Shop.md)
- [Status](Content-Status.md)
- [Title](Content-Title.md)
- [Weather](Content-Weather.md)

### characters
- [Characters](Character.md)

### base data

- [Maps](Maps.md)
- [Game Data](Data.md)
    - EXP Table
    - ClassJobs
    - Cabinet
    - Armoire
    - Grand Companies
    - Patch List (XIVDB Built in patch system)
    - *... request more ...*

### Lodestone Information + Dev Tracker

- Lodestone Data - http://xivdb.com/assets/lodestone.json
- Dev Tracker - http://xivdb.com/assets/devtracker.json

Both the lodestone data and the dev tracker update every 5 minutes and are always in English. You can use these on your sites freely.

### Examples

- [chat bot type scenario](https://codepen.io/viion/full/xLYELO/)

---

## wip
*No particular order*

- PHP SDK
- Javascript SDK
- Map Embeds
- Add Custom Gearsets to the API
- Add Shopping Carts to the API
- Providing Achievement Ranking data to the API
- Provide more information for characters
- Provide schema column selection for core data

---

## routing
> API Endpoint: `https://api.xivdb.com/`

Accessing content pages from the API is as simple as putting `api.` infront of the URL, here are some examples:

- `http://xivdb.com/item/1675/curtana` 
    - --> `http://api.xivdb.com/item/1675/curtana`
- `http://xivdb.com/instance/43/the+antitower` 
    - --> `http://api.xivdb.com/instance/43/the+antitower`
- `http://xivdb.com/character/730968/premium+virtue/phoenix` 
    - --> `http://api.xivdb.com/character/730968/premium+virtue/phoenix`

The Names (and for characters: Server) is optional and not required, eg:

- `http://api.xivdb.com/item/1675/curtana` 
    - OR `http://api.xivdb.com/item/1675`
- `http://api.xivdb.com/character/730968/premium+virtue/phoenix` 
    - OR `http://api.xivdb.com/character/730968`

---

## global commands
> `language=[LANG]`

> `[LANG]` **Options:** English `en`, German `de`, French `fr`, Japanese `ja`

Set the language for the data. This is primarally for content pieces (Character data is mostly English for now, more on that in the Character section), here are some examples:

- German: https://api.xivdb.com/item/1675?language=de
- French: https://api.xivdb.com/item/1675?language=fr
- Japanese: https://api.xivdb.com/item/1675?language=ja

**language during search/filters**

Sometimes you may not always know what the language is. Search content will often fetch results in all 4 languages for named content, eg: `name_en`, `name_fr`, `name_de`, `name_ja` in this case you can use the placeholder `{lang}` and the system will handle it for you, eg: `name_{lang}` or `description_{lang}`


> `pretty=1`

Enables a pretty view for the JSON. This is very helpful for debugging and reading what is in the response, eg:

- https://api.xivdb.com/item/1675?pretty=1

**Before:** 
```json
{"achievements":null,"action":0,"aetherial_reduce":0,"attributes_base":{"auto_attack":34.02,"auto_attack_hq":34.02,"block_rate":0,"block_rate_hq":0,"block_s ...
```

**After:**
```json
{
    "achievements": null,
    "action": 0,
    "aetherial_reduce": 0,
    "attributes_base": {
        "auto_attack": 34.02,
        "auto_attack_hq": 34.02,
        "block_rate": 0,
        "block_rate_hq": 0,
```

---

## protocol notes
Both `http` and `https` are supported. The reason for this is because the API isn't intended to be crawled by Google or used in SEO it is setup to make it easy for developers to jump in. 

Accessing `https` urls in some languages requires extra code or SSL verification and it might be simplier to stick to the `http` version. If you're using the API in a frontend library (eg: Javascript) and your site is behind an SSL certificate, you will have to use the `https` endpoint.

*There is no sensitive data on the API and you can only retrieve game related data, nothing regarding members, comments or screenshots.*

---

## rate limiting
There are no strict limits on the API at this time, however this does not excuse bad coding practices. Do not query the API in a `for/foreach/while` loop and leverage caching, game content updates every patch so it is not needed to query every time!

The API sits behind Redis and should be fairly responsive, think about what kind of calls you will be doing to the API and what kind of data you need. 

If you are looking for all of the game data then you may find it more useful to extract the CSV's yourself, Information on that can be found here: https://github.com/viion/XIV-Datamining

---

## support

If you need help with the API please don't hesitate to contact me, I am happy to answer all questions, fix any issues or add in additional information. Just bcause some data doesn't exist doesn't mean I can't add it!

Please join the Discord: https://discord.gg/6XT7FTJ and there is a channel called `web-dev` for API Stuff

---

# rate limit

The XIVDB has a 15 requests/second rate limit before it will begin denying requests. Please code respectfully, this means no `foreach` or `while` loops firing off requests, either use recurrsion, promises or callbacks.

Here is a Javascript gist that shows bad/good query code:

- https://gist.github.com/viion/d30684c402995b9f4b91d2e95faf1ef4
