# CRYSTALISYS

An old-school Final Fantasy style JRPG for **AuroraOS**.

The Dawn Crystal above the village of Lumen has gone dark. Four heroes (REX, MIRA, LYRA and ORIN) set out to find its lost shards and relight it.

## Controls

| Button | Walking around | Menus and battle |
| --- | --- | --- |
| D-pad / Circle pad | Move | Move the cursor |
| A | Talk, open chests, confirm | Confirm |
| B | Hold to run (twice the speed) | Cancel / go back |
| X or START | Open the menu | n/a |
| L / R | n/a | Switch hero, shop tab, or INFO / quest-log page |
| HOME | Exits and saves | n/a |

Walking uses real elapsed time, so speed is the same at any frame rate.

## Field menu

Open it with X or START.

- **ITEM**: use potions, ethers, tents and so on.
- **MAGIC**: cast healing and support spells outside battle.
- **EQUIP**: change a hero's weapon, head, body, arms and legs. The screen compares the new piece with the old one.
- **WARP**: jump to any Waystone you have unlocked (see below).
- **STATUS**: stats, level and class for each hero.
- **QUESTS**: a two-page log with the main story and side quests, plus a "next up" hint.
- **INFO**: author, contact and GitHub page (edit the `INFO_*` defines near the top of `main.c`, or put an `info.txt` in the app folder with five lines: author, contact, GitHub, website, message; use `-` for a blank line).
- **SAVE**: write your game.
- **CLOSE**.

## Battle

Classic turn-based fights. Every hero picks a command, then the round plays out fastest-first.

- **FIGHT**: attack with your weapon.
- **SKILL / MAGIC**: the class command. Knights, Thieves, Monks, Dragoons and Samurai get skills; the mages get spells.
- **ITEM**: use something from the bag.
- **DEFEND**: take less damage this round and act first.
- **RUN**: try to flee.

Some enemies resist or are weak to fire, ice, bolt and holy. Bosses also have special moves and some change form mid-fight.

## Classes

Eight classes: **Knight, Thief, White Mage, Black Mage** from the start, and **Monk, Dragoon, Red Mage, Samurai**, which the Class Master in Frostholm teaches. Any hero can switch to any class you have unlocked. Level and EXP stay the same, and gear that no longer fits goes into your bag rather than being sold.

## Gear

- Weapons are spread across shops, chests and bosses, and each is limited to the classes that can use it.
- There are four armor slots: **head, body, arms, legs**. Each piece adds defense and often small STR / MAG / SPD bonuses, so you can min-max a build.
- Spare gear lives in the bag. Shops have a tab for each slot plus a SELL tab.
- Chests equip the item on the first hero who gets a real upgrade from it. Otherwise it goes into the bag.

## Towns, inns and Waystones

- Towns: **Lumen, Frostholm, Tidewick, Emberfall**, each with a shop and an inn.
- **Inns** have a blue roof, an INN sign, a glowing door and a bobbing gold arrow. The bottom screen also points you toward the nearest one. Resting restores HP and MP and saves the game.
- **Waystones** unlock the first time you enter a town or dungeon: Lumen, Gloam Cavern, Frostholm, Frostpeak Keep, Tidewick, Emberfall, Mire Crypt, Cinder Mines and Umbral Spire. Use **WARP** in the menu to pick one from a world map.

## The story in brief (spoilers lightly)

1. **Gloom Wyrm** in Gloam Cavern drinks the Crystal's light. Defeating it opens the frozen north.
2. **The Hollow King** in Frostpeak Keep was once King Aldric the Bright.
3. **The Crypt Lich** guards a shard in the Mire Crypt.
4. **Vesper, the Dusk Regent** waits at the top of the Umbral Spire. It is a two-form final fight.

There are also side quests: a lost boy in the first cavern, a sailor's missing pearl, and a smith who needs phoenix feathers. Check the QUESTS page if you are stuck.

## Saving

The menu has SAVE, inns save for you. The save file is `save.dat` in the app's data folder.

## Tips

- Rest at an inn before every boss.
- Frost enemies melt to fire; the dead hate holy magic.
- Check shop SELL tabs and your bag after changing classes.
- Keep a TENT in reserve for dungeon runs.
