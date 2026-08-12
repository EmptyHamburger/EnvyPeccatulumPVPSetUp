# Configure your PVP Encounter

Assuming you have downloaded the `PVP Encounter Template` from the `Identity to Envy Peccatulum` thread
Open `PVPEncounterTemplate/custom_encounters/PVP/encounter.json`

Ill go with most important stuffs first

1. Max sinner deployment
Edit the `max` value in `participantInfo` to set the maximum number of Sinners you want to deploy for combat (Others will be in backup)

2. Identities for Envy Peccatulum side
The `unitList` is where you place identities that will be instantly deployed when entering the encounter
The `subUnitList` is where you place your backup identities
Inside `unitList`, there are 6 units by default
Let's look at an example:
```json
{
    "unitID": 2000010216,
    "unitLevel": 100,
    "unitCount": 1,
    "unitSyncLevel": 4,
    "isHide": false
}
```
`unitID`: The unit's ID
`unitLevel`: The unit's level
`unitCount`: how many unit there are
`unitSyncLevel`: The unit's uptie level
`isHide`: ignore this

The format is exactly the same for `subUnitList` you if want to add a backup identity
Be aware that the deployment order for the Envy Peccatulum side reads from top to bottom. For ex, the identity placed first in the `unitList` will have deployment order of `1` and this goes on until the end of the list then the deployment order is continued in `subUnitList`

To find the identity's ID you want, open a code editor software and navigate to `YourLetheFolder/BepInEx/plugins/Lethe/dumpedData/limbus_data/personality`

Here you can find every vanilla identity ID in the game. In the screenshot, you can see the ID for `LCB Yi Sang` is `10101`
However, when inputing this ID number into `unitID`, it gonna be `2000010101` (Which is `2000000000` + `10101`, or 2 billions + the vanilla ID)

3. Map & Background Music
In `battleMapInfo` you can edit the map's size and which map you want (Default is Kind in Binds map)
In `bgmList` you can set own bgm music (Default is Canto 9 Boss Theme 2 - Lucio/Valencina fight)