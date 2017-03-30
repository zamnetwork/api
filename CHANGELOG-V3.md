# WIP CHANGELOG V3

These are work-in-progress change logs for version 3 of the XIVDB API

## Major changes


## Minor changes

- All empty/null responses should now be "false".
- All lists should now be an Array (not an Object).
- Patch data will only be on primary content at the top level.
- Data that is intended to be an array will be an empty array when no data available.

## Minor additions

- It is now possible to exclude content pieces from top level datsets, eg:

> api.xivdb.com/item/5056?exclude=recipe_crafts_into,recipe_created_from

This will exclude `recipe_crafts_into` and `recipe_created_from` data if you do not need it, allowing for a smaller payload of data.


## Data removed


## Data added


## Data changed

- HQ values will no longer be included when they're the same of the NQ value (Thus no HQ benefit).
