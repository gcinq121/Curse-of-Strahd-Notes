```dataview
TABLE WITHOUT ID link(file.name) AS "Name", encounterDate AS "Encounter Date", encounterLocation AS "Encounter Location", lastSeen AS "Last Seen", alive AS "Alive", info AS "INFO"
WHERE (type = "NPC") AND (alive != null)
SORT file.mtime DESC
```