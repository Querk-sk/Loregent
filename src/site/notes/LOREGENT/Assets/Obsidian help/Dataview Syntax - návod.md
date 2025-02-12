---
{"dg-publish":true,"permalink":"/loregent/assets/obsidian-help/dataview-syntax-navod/"}
---

## Table
Urobí tabuľku.  V tomto príklade dole sú použité " ,,, ", to preto, lebo markdown robí hovadinu, keď tam dám originál príkaz (tie opačné dĺžne ( alt + ý )). 

- Keď chceš urobiť viacero stĺpcov, napíš tam parametre, ako "author"
- Keď chceš premenovať stĺpec, napíš AS "Creator" (alebo niečo iné)
{ #dffee3}


```
,,, dataview
TABLE author AS Creator, genre AS Žáner
```

Data view TABLE

| File |
| ---- |

{ .block-language-dataview}

## Task
Data view TASK (všetko čo je škrtacie políčko - `[ ]` - tak to všetko zoradí do tohto zoznamu)

- [ ] a ?
- [x] Write
- [x] Check
- [x] Translate
- [ ] Checking translation <<<<-- now : [[LOREGENT/1 - ROLEPLAY/03 CHARACTER/attributes skills talent/RPG - Skills STR\|RPG - Skills STR]]
- [ ] Write <<<<<<------- The Land of Time (and Lands overall)
- [ ] Check
- [ ] Translate
- [ ] Write
- [ ] Check
- [ ] Translate
- [ ] Write
- [ ] Check
- [ ] Translate
- [ ] Write
- [ ] Check
- [ ] Translate
- [ ] Write a short story for testing purposes

{ .block-language-dataview}
## List

Data view LIST (platí všetko ako pri Table)


{ .block-language-dataview}

## Filtrovacie príkazy

### FROM
Filtruje výstup na základe priečinku alebo tagu (doslova "odkiaľ")

- berie názov priečinku, musí to mať ale ""  ( "0 - Testing Obsidian" )
	- Berie aj sub priečinok "0 - Testing Obsidian/Podpriečinok "
- berie tag ( # básničky (( len musí to byť bez medzere, ale keď to dám sem , tak mi to zaradí do básničiek, ale chápeme sa))
- Outgoing links `outgoing([[Zdroje/Markup language/Dataview|Dataview]])`
- FROM podporuje AND, ďalej OR, alebo aj exclude (napr. chcem vidieť všetky tags okrem básničky , tak dám " - " pred básničky)

### WHERE
Filtruje výstup na základe tagov, alebo iných značiek (doslova " kde ")

- file.name = "Atomic Habits"  ( je presne Atomic Habits )
- file.name != "Atomic Habits"  ( vypíš všetko, okrem Atomic Habits )
- file.size >2000 ( napíše všetky súbory, ktoré sú väčšie než 2000 b )
- contains(author, "Gilian Freudman") (napíše všetky súbory, ktoré majú v sebe Giliana)

### SORT
Zoradí podľa vstupu ( SORT file.name `asc` pre vzostupné a `desc` )

| File | file.name | file.size |
| ---- | --------- | --------- |

{ .block-language-dataview}

### Built-in data
[Dataview in Obsidian: A Beginner's Guide - Obsidian Rocks](https://obsidian.rocks/dataview-in-obsidian-a-beginners-guide/)

| Field Name             | Description                                                                                                                                                                     |
| ---------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `file.name`            | The file name as seen in Obsidians sidebar.                                                                                                                                     |
| `file.folder`          | The path of the folder this file belongs to.                                                                                                                                    |
| `file.path`            | The full file path, including the files name.                                                                                                                                   |
| `file.ext`             | The extension of the file type; generally `md.                                                                                                                                  |
| `file.link`            | A link to the file.                                                                                                                                                             |
| `file.size`            | The size (in bytes) of the file.                                                                                                                                                |
| `file.ctime` with Time | The date that the file was created.                                                                                                                                             |
| `file.cday`            | The date that the file was created.                                                                                                                                             |
| `file.mtime` with Time | The date that the file was last modified.                                                                                                                                       |
| `file.mday`            | The date that the file was last modified.                                                                                                                                       |
| `file.tags`            | A list of all unique tags in the note. Subtags are broken down by each level, so `#Tag/1/A` will be stored in the list as `[#Tag, #Tag/1, #Tag/1/A]`.                           |
| `file.etags`           | A list of all explicit tags in the note; unlike `file.tags`, does not break subtags down, i.e. `[#Tag/1/A]`                                                                     |
| `file.inlinks`         | A list of all incoming links to this file, meaning all files that contain a link to this file.                                                                                  |
| `file.outlinks`        | A list of all outgoing links from this file, meaning all links the file contains.                                                                                               |
| `file.aliases`         | A list of all aliases for the note as defined via the [YAML frontmatter](https://help.obsidian.md/How+to/Add+aliases+to+note).                                                  |
| `file.tasks`           | A list of all tasks (I.e., `\|[ ] some task`) in this file.                                                                                                                     |
| `file.lists`           | A list of all list elements in the file (including tasks); these elements are effectively tasks and can be rendered in task views.                                              |
| `file.frontmatter`     | Contains the raw values of all frontmatter in form of `key \|value` text values; mainly useful for checking raw frontmatter values or for dynamically listing frontmatter keys. |
| `file.day`             | Only available if the file has a date inside its file name (of form `yyyy-mm-dd` or `yyyymmdd`), or has a `Date` field/inline field.                                            |
| `file.starred`         | if this file has been starred via the Obsidian Core Plugin “Starred Files”.                                                                                                     |

## Dataviewjs Examples
[Dataviewjs Examples - Fork My Brain (nicolevanderhoeven.com)](https://notes.nicolevanderhoeven.com/obsidian-playbook/Obsidian+Plugins/Community+Plugins/dataview/Dataviewjs+Examples)
