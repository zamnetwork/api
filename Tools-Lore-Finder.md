# Lore Finder

|Endpoint|
|---|
|`http://api.xivdb.com/lore-finder`|

You can use the API to search lore! This uses the same tool that can be found here: http://xivdb.com/lore-finder

Currently you can search:
- Quest Dialogue
- Speech Bubbles
- Content Descriptions
- Instance Text Data
- NPC Shouts
- Public Content Data

## parameters

> `loresearch=[string]`

eg: `http://api.xivdb.com/lore-finder?loresearch=kupo`

Search all lore material for the word "kupo"

**RESPONSE SNIPPET**

```json
{
    "string": "kupo",
    "totals": {
        "xiv_quests_to_text": 93075,
        "xiv_balloons": 3383,
        "xiv_contents_description": 145,
        "xiv_instances_text_data": 1693,
        "xiv_npc_yells": 4228,
        "xiv_public_content_text_data": 144
    },
    "results": {
        "xiv_quests_to_text": [
        
        ],
```
