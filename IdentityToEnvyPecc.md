# Configure your Envy Peccatulum EGOs

Assuming you have downloaded `config.json` from the `Identity to Envy Peccatulum` thread, open the file

```json
// E.G.O
{
    "DefaultEgo": [ // [EGO ID, Uptie Level] (EGO ID = 0 means no EGO will be provided). Ex: [21001, 3] -> Branch of Knowledge, Uptie 3
        [[20101, 1], [0, 1], [0, 1], [0, 1]], // Yi Sang
        [[20201, 1], [0, 1], [0, 1], [0, 1]], // Faust
        [[20301, 1], [0, 1], [0, 1], [0, 1]], // Don Quixote
        [[20401, 1], [0, 1], [0, 1], [0, 1]], // Ryoshu
        [[20501, 1], [0, 1], [0, 1], [0, 1]], // Meursault
        [[20601, 1], [0, 1], [0, 1], [0, 1]], // Hong Lu
        [[20701, 1], [0, 1], [0, 1], [0, 1]], // Heathcliff
        [[20801, 1], [0, 1], [0, 1], [0, 1]], // Ishmael
        [[20901, 1], [0, 1], [0, 1], [0, 1]], // Rodion
        [[21001, 1], [0, 1], [0, 1], [0, 1]], // Sinclair
        [[21101, 1], [0, 1], [0, 1], [0, 1]], // Outis
        [[21201, 1], [0, 1], [0, 1], [0, 1]] // Gregor
    ],
    "SpecificIdEgos": [
        // Here a template for Shi Faust
        // -------------- COPY FROM LINE 20 TO LINE 23----------------
        // {
        //     "id": 10213,
        //     "ego": [[20201, 2], [20205, 3], [20209, 1], [20206, 4]]
        // }
        // -----------------------------------------------------------
        // Explaination:
        // [20201, 2] => ZAYIN: 'Representation Emitter', Uptie 2
        // [20205, 3] => TETH: '9:2', Uptie 3
        // [20209, 1] => HE:  'Command : Meltdown', Uptie 1
        // [20206, 4] => WAW: 'Everlasting', Uptie 4
    ]
}
```

The `DefaultEgo` section is the EGO list applied for every identity, each line corresponds to a specific Sinner
Example:
```json
[[20101, 1], [0, 1], [0, 1], [0, 1]], // Yi Sang
```
This line means that all all Yi Sang identities will have the `Crow's Eye View ` Uptie 1 EGO equipped and no TETH, HE and WAW EGOs equipped

The `SpecificIdEgos` section allows you to equip specific EGOs for specific identities
Example:
```json
{
    "id": 10213,
    "ego": [[20201, 2], [20205, 3], [20209, 1], [20206, 4]]
}
```
This means the `Shi Assoc. East Section 3 Faust` identity will have the following EGOs equipped:
- 'Representation Emitter', Uptie 2
- '9:2', Uptie 3
- 'Command : Meltdown', Uptie 1
- 'Everlasting', Uptie 4

The file already explained pretty much how this works but you may have trouble finding the correct EGO IDs
Open `YourLetheFolder/BepInEx/plugins/Lethe/dumpedData/limbus_locale/egoList.json`. Here you can find every EGO ID that exists in the game