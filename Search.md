# search

|Endpoint|
|---|
|`https://api.xivdb.com/search`|

The search allows you to search! You can find information for all main content types as well as characters. Search provides some small additional fields that can help you present user friendly views. The API also has an extremely robust filter system which is easy to grow (if you need more filters, let me know!)

The search API is best used for:
- Wildcard Content finding
- Character searching
- Visually pleasing search results for frontend applications

It is not good for:
- Rapid fire searching
- Auto-completion

---

## quick tip

If you are building an application that requires the search then the best way to view what kind of things you can do is to use your browsers built in Developer Tools. If you go to the XIVDB's home page, open up developer tools, go to the: `Network` tab, filter requests by `XHR` and then click on one of the search options in XIVDB you will see the request. You can then click on that request to see the kinds of parameters that were sent.

![example](http://i.imgur.com/fQDKtQj.png)

You can then play around with the filters on the site and view the `Query String Parameters` to get a real-time demo of how it's used!

---

## core parameters
> `string=[some string]`
eg: `string=allagan braclets of aiming`

Search titles for some piece of content, use this to find item names, instance names, or even character names! For titles this will search both Male and Female titles.
- **Character limit:** 2

> eg: `string=maiming,belt`

Using a comma will split words by "AND", eg: `maiming,belt` will return stuff with `maiming` AND `belt` in the name, eg:
- Heavy Metal Plate **Belt** of **Maiming**
- Hero's **Belt** of **Maiming**

> eg: `string=maiming/belt`

Using a forward slash will split words by "OR", eg: `maiming/belt` will return stuff with `maiming` OR `belt` in the name, eg: 
- Diabolic **Belt** of Casting (not maining)
- Filibuster's Heavy Boots of **Maiming** (not a belt)

> `one=[type]`
`one=items`

Filters a specific content type, the list of content types are:

|Types|||||||
|---|---|---|---|---|---|---|
|items|recipes|quests|actions|instances|achievements|fates
|leves|places|gathering|npcs|enemies|emotes|status
|titles|minions|mounts|weather|characters

If ommited or set to "All", all content types are searched.

> `order_field=[field]`

Set the field in which to order the content by. All content has the field `id`, `name` and `patch`. `name` is special in that is the name based on your current language. So if you provide the parameter `language=fr` then ordering by `name` will be ordered by French names.

Possible fields: [Search Orders](Search-Order.md)

> `order_direction=[asc|desc]`

Provide the direction for the results, this will either by: `ASC` or `DESC`, (case insensitive, can be lower case)

> `page=[x]`

Which page to start on, if you implement pagination on your use-case then you will need to provide a page. When ommited it defaults to `1`

> `limit=[x]`

Limit the number of results to return from the API.
- **Maximum:** 90

> `strict=[on|off]`

Toggle search strict mode, by default all string searches are wildcard and search both sides, for example:
- OFF: `aim` would find items with the word: M**aim**ing---
- ON: `aim` would only find items starting with Aim---

The purpose of this is if you really need to use the search for auto-complete, then `strict=ON` would make it more obvious to the user. It also provides a faster response than without it for smaller values.

## commands
> `string=!patch+{patch version}`

This is a special command in that it will return all new content for a specific patch, you can find the list of patches here: http://api.xivdb.com/data/patchlist?pretty=1, for example:
- https://api.xivdb.com/search?string=patch+3.5

## filters

There are many filters for all the different types of content

**STRUCTURE**
> `{filter}|{operator}`

For example:
- `level|gt=X` means `Level Greater Than X`
- `level|lt=X` means `Level Less Than X`
- `level|et=X` means `Level Equal To X`

Some variables only have an equal to because they're boolean based, eg:

- `is_pvp=1` means `Items that are PVP`

**CONTENT FILTERS**

### Achievements
```
points|et
achievement_category|et
item
title
patch|et
```
### Actions
```
level|gt
level|lt
action_category|et
can_target_dead
is_target_area
can_target_self
can_target_party
can_target_friendly
can_target_hostile
is_pvp
patch|et
classjobs
classjobs_andor
```
### Characters
```
server|et
achievements_public
```
### Emotes
```
patch|et
```
### Enemies
```
patch|et
```
### Fates
```
class_level|gt
class_level|lt
class_level_max|gt
class_level_max|lt
placename|et
patch|et
```
### Gathering
```
level|gt
level|lt
level_view|gt
level_view|lt
```
### Instances
```
level|gt
level|lt
level_sync|gt
level_sync|lt
item_level|gt
item_level|lt
item_level_sync|gt
item_level_sync|lt
instance_content_type|et
content_roulette|et
is_echo_default
is_echo_annihilation
new_player_bonus
content_roulette
alliance
is_in_duty_finder
patch|et
```
### Items
```
level_item|gt
level_item|lt
level_equip|gt
level_equip|lt
item_ui_category|et
item_ui_kind|et
item_series|et
materia_slot_count|et
rarity|et
patch|et

source|et
    Values:
    =achievement
    =craftable
    =instance
    =instance_reward
    =instance_chest
    =quest
    =enemy
    =shop
    =gathering

attributes
    Group a set of attributes in the format: ID|OPERATOR|VALUE|HQ
    eg: 22|gt|5|0,25|gt|10|1
        Attribute 22 Greater Than 5 NQ
        AND|OR
        Attribute 25 Greater Than 10 HQ

attributes_andor
    Set the AND|OR for attribute filters.
    
classjobs
    A list of class/job ids
        eg: 2,17,24,26
            Pugilist, Arcanist, White Mage, Botanist    
        
classjobs_andor
    Set the AND|OR for classjobs filter.
classjobs_exclusive
```
### SearchLeves
```
class_level|gt
class_level|lt
placename|et
patch|et
```
### SearchMinions
```
patch|et
```
### SearchNPC
```
patch|et
```
### SearchPlacenames
```
patch|et
```
### SearchQuests
```
class_level_1|gt
class_level_1|lt
patch|et
```
### SearchRecipes
```
level|gt
level|lt
level_view|gt
level_view|lt
can_quick_synth
can_hq
level_diff|et
recipe_element|et
patch|et
classjobs
classjobs_andor
```
### SearchStatus
```
patch|et
```
### SearchTitles
```
patch|et
```
### SearchWeather
```
patch|et
```
