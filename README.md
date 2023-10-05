# pfQuest

Quest helper AddOn made by Shagu. This AddOn helps players to find several ingame objects and quests. The addon reads questobjectives, parses them and uses its internal database to plot the found matches on the world- and minimap. It ships with a GUI to browse through all known objects. If one of the items is not yet available on your realm, you'll see a [?] in front of the name.

---

pfQuest is the successor of ShaguQuest and has been entirely written from scratch. In comparison to ShaguQuest, this addon does not depend on any specific map- or questlog addon. It's designed to support the default interface aswell as every other addon. In case you experience any addon conflicts, please add an issue to the bugtracker.

## Controls
- To change node colors on the World Map, **click** the node.
- To remove previously done quests from the map, **\<shift\>-click** the quest giver on the world-map
- To temporarily hide clusters on the world-map, hold the **\<ctrl\>-key**
- To temporarily hide nodes on the mini-map, hover it and hold the **\<ctrl\>-key**
- To move the minimap-button, **\<shift\>-drag** the icon
- To move the arrow, **\<shift\>-drag** the frame

## Addon Memory Usage
The addon ships an entire database of all spawns, objects, items and quests and therefore includes a huge database (~80 MB incl. all locales) that gets loaded into memory on game launch. However, the memory usage of pfQuest is persistent and does not increase any further over time, so there's nothing bad on performance at all. Depending on the download you pick (especially the full packages), you might see a message that warns you about an addon consuming too much memory. To get rid of that warning, you can set the addon memory limit to `0` which reads as `no limit`. This option can be found in the [character selection screen](https://i.imgur.com/rZXwaK0.jpg).

## Auto-Tracking
The addon features 4 different modes that define how the new or updated questobjectives should be handled. Those modes can be selected on the dropdown menu in the top-right area the map.

## Option: All Quests
Every quest will be automatically shown and updated on the map.

## Option: Tracked Quests
Only tracked quests (Shift-Click) will be automatically shown and updated on the map.

## Option: Manual Selection
Only quest objectives that have been manually displayed ("Show"-Button in the Questlog) will be displayed.
Completed quest objectives will be still automatically removed from the map.

## Option: Hide Quests
Same as "Manual Selection" and in addition to that, Quest-Givers won't be shown automatically.
Also completed quest objectives will remain on the map. This mode won't touch any of the map nodes created.

## Database Browser
The database GUI allows you to bookmark and browse through all entries within the pfQuest database. It can be opened by a click on the pfQuest minimap icon or via `/db show`. The browser will show a maximum of 100 entries at once for each tab. Use your scrollwheel or press the up/down arrows to go up and down the list.

## Questlog Buttons
The questlog will show 4 additional buttons on each quest in order to provide easy manual quest tracking. Those buttons can be used to show or hide individual quests on the map. Those buttons won't affect the entries that you've placed by using the database browser.

**Show**  
The "Show" button will add the questobjectives of the current quest to the map.

**Hide**  
The "Hide" button will remove the current selected quest from the map.

**Clean**  
The "Clean" button will remove all nodes that have been placed by pfQuest from the map.

**Reset**  
The "Reset" button will restore the default visibility of icons to match the set values on the map dropdown menu (e.g "All Quests" by default).

# Chat/Macro CLI

The addon features a CLI interface which allows you to easilly create macros to show your favourite herb or mining-veins. Let's say you want to display all **Iron Deposit** deposits, then type in chat or create a macro with the text: `/db object Iron Deposit`. You can also display all mines on the map by typing: `/db mines`. This can be extended by giving the minimum and maximum required skill as paramter, like: `/db mines 150 225` to display all ores between skill 150 and 225. The `mines` parameter can also be replaced by `herbs`, `rares`, `chests` or `taxi` in order to show those instead. If `/db` doesn't work for you, there are also some other aliases available like `/shagu`, `pfquest` and `/pfdb`.

![image](https://github.com/endless-addons/pfQuest/assets/46463908/711b0465-bcf7-49c3-8558-617ee436c97d)
