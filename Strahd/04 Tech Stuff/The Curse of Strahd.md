| ![[barovia-map.png\|hs-sm+wm-sm+center]] | ![[npcScreen.png\|hs-sm+wtall+center]] |
| ------------------------------------------ | ---------------------------------------- |
| [[03 Barovia\|Barovia]]                    | [[02 NPC.md\|NPC]]                   |


>[!infobox]
># Session Journals
>```dataview
TABLE WITHOUT ID link(file.name) AS "Session Date", location AS "Where", oneLiner AS "One Liner"
WHERE type = "Session Journal"
AND file.name != "Session Journal"
SORT file.sessionDate ASC

### Recently Modified
```dataview
TABLE WITHOUT ID
link(file.path, file.folder + "/" + file.name) AS "Note",
file.mtime AS "Last Modified"

FROM ""
WHERE file.mtime >= date(today) - dur(30 days)
AND file.name != this.file.name
SORT file.mtime DESC
LIMIT 10
```

