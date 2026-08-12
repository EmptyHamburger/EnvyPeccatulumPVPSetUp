# Custom settings in EnvyPeccatulumPVP.dll

Open `EnvyPeccatulumPVP.json` file that you placed in your `YourLetheFolder/BepInEx/plugins` folder
```json
{
  "Active": false,
  "SpValue": [
    0,
    0,
    0,
    0,
    0,
    0,
    10,
    15,
    20,
    20,
    30,
    30
  ],
  "ClashWin": 5,
  "ClashWinMultiplier": 0,
  "ClashLose": -5,
  "ClashLoseToLowerSPEnemy": -5,
  "Unopposed": 3,
  "AllyKilled": 10,
  "EnemyKilled": 10,
  "EnemyKilledByAlly": 5,
  "GateSPMin": -45,
  "GateSPMax": 45
}
```
These settings are not activated by default. To use them, set `Active` to `true`
`SpValue` determines the SP value your identities receive upon entering the encounter for the first time (SP back mechanic but works for every deployment order). This works for both the Sinner and Envy Peccatulum sides

All other settings apply to every unit on field regardless of their their faction
1. `ClashWin` and `ClashWinMultiplier` are for this vanilla sanity script

<img width="400" height="72" alt="ClashWinAndMultiplier" src="https://github.com/user-attachments/assets/d7107ec8-8258-46d6-853c-3725a17c2333" />

Default:
- Increases after winning a Clash based on Clash count
- (Base Value is 5, raised by 0% per Clash count after 1)

2. `ClashLose`: How much SP a unit gains/loses when losing a Clash
3. `ClashLoseToLowerSPEnemy`: How much SP a unit will gains/loses when losing a Clash against target with a lower SP value
4. `Unopposed`: How much SP a unit will gains after finishing an unopposed attack
5. `AllyKilled`: How much SP a unit will gains after an ally is killed
6. `EnemyKilled`: How much SP a unit will gains after an enemy is killed
7. `EnemyKilledByAlly`: How much SP a unit will gains after an enemy is killed by an ally
8. `GateSPMin`: A units' SP value cannot fall below this threshold
9. `GateSPMin`: A units' SP value cannot rise above this threshold
