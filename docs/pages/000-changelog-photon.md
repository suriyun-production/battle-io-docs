# Changelog (PUN2)
**I decided to make all important parts to be an open source projects, so you won't have to buy this one, you can find source codes [here](https://github.com/insthync?tab=repositories&q=io-core&type=&language=&sort=)**

## 1.30 (2022-07-04)
- Update Purchasing integration.
- Update Facebook SDK integration.
- Update Google Play Games Service integration.
- Update PlayFab SDK integration.
- Setup events to update purchased items (You won't have to set it by yourself anymore).
- Change demo's currency ID from `GOLD` to `GO` to make it compatible with PlayFab.

## 1.29b (2022-02-26)
- Update to Unity version 2020.3.26f1.
- Fix score and kills not being counted properly.

## 1.29 (2021-10-22)
- Fix character cannot being pushed by forces.
- Fix character cannot change weapon by attributes.
- Fix status effects not being applied properly.
- Fix Playfab data exporter not export bundles.

## 1.28 (2021-08-07)
- Reduce packet size.
- Add blocking action.

## 1.27b (2021-04-05)
- Fix null data break update loop.
- Fix unsynced aim position.
- Don't update aim position for non-owning characters.

## 1.27 (2021-03-29)
- Improve character movement, now it has to attached `CharacterMovement` component to `CharacterEntity` when you attaches `CharacterMovement` component, you have to set `CharacterController` settings to cover your character and you have to set attached colliders to be trigger collider.
- Add third person view mode, you have to change `FollowCamera` component which usaully attached to main camera to `FollowCameraControls` component.
- Add `ViewMode` settings to `CharacterEntity`, you can set it to `TopDown` and `ThirdPerson`.
- Add `TopDownViewModeSettings` it will be applied to `FollowCameraControls` and main camera when `ViewMode` is `TopDown`.
- Add `ThirdPersionViewModeSettings` it will be applied to `FollowCameraControls` and main camera when `ViewMode` is `ThirdPerson`.

## 1.26c (2020-12-08)
- Remove automatic leave room from gameplay rule.
- Hide room from lobby list when match end.
- Fix wrong player's ranking when match end.

## 1.26b (2020-11-30)
- Rework on team system, it won't use Photon's team utility anymore.
- Fix wrong bots adjusting amount when player join or leave rooms.

## 1.26 (2020-11-07)
- Change RPC function usages from `photonView.RPC("function", player, param1, param2, param3)` to `photonView.TargetRPC(function, player, param1, param2, param3)`.
- Change RPC function usages from `photonView.RPC("function", RpcTarget.All, param1, param2, param3)` to `photonView.AllRPC(function, param1, param2, param3)`.
- Change RPC function usages from `photonView.RPC("function", RpcTarget.Others, param1, param2, param3)` to `photonView.OthersRPC(function, player, param1, param2, param3)`.
- Change RPC function usages from `photonView.RPC("function", RpcTarget.MasterClient, param1, param2, param3)` to `photonView.MasterRPC(function, player, param1, param2, param3)`.
- Fix teams are not spawning in designated team spawn areas.
- Fix teams are not spawning the correct amount for each team. If its 6 players, sometimes one team has 4, the other 2.
- Fix bug when the master leaves then rejoins a room, more bots are spawned than the limit.
- Improve how to instantiate damage entity, now it will simulate immediately while playing action animation, not have to wait for instantiate networking messages.

## 1.25 (2020-07-02)
- Change to move characters by changes transform's position, rigibody will be used to applies force.
- Add `ExplosionForce` and `ExplosionForceRadius` settings to `Damage Entity` it will applies to force character when damage entity hit or explode.
- Add `DivideSpreadedDamageAmount` if this is `TRUE`, damage amount will be divided by amount of spread damages.

## 1.24 (2020-05-08)
- Fix team death match kill count and score don't reset when start new match
- Fix black fade not fade out when start game sometime
- Fix kill count / score won't increase after character killed by `StatusEffectEntity`

## 1.23b (2020-04-16)
- Fix stack overflow while playing Battle Royale
- Add `NO_IAP` and `NO_ADS` predefined to disable IAP or ADS

## 1.23 (2020-04-15)
- Update PUN2

## 1.22b (2020-02-16)
- Fix invalid adjusting BOTs amount when players enter or exit the game

## 1.22 (2020-02-12)
- Add `StatusEffectEntity` which can set to `DamageEntity` or `SkillData` as a buffs or nerfs to increase or decrease character's stats.
- Fix null exceptions occuring after enter or exit `HideArea`.

## 1.21
- Fix invalid weapon model's damage launch transform position.
- Implement NavMesh to BotEntity, Bot will find paths from NavMesh if there is baked NavMesh in the scene. Developers don't have to add NavMeshAgent to BotEntity.
- Bots can dash.
- Bots can use skills
- Bots can increase their attributes.

## 1.20b
- Fix hide area bugs
- Fix cannot start game in offline mode
- Fix invalid bot count

## 1.20
- Add `HideArea`, developer can attach this component to grasses which will be used to hide characters
- Fix invalid add bot state when switch master client

## 1.19d
- Remove transforms from Photon View → Observe List
- Avoid null exception when there is no head to select
- Add plane to Battle Royale demo

## 1.19c
- Fix invalid GameInstance and UIMainMenu execute order

## 1.19b
- Fix bought items won't be saved

## 1.19
- Add Playfab integration demo

## 1.18
- Fix home scene loading while application quit
- Add codes to support Playfab integration project (https://github.com/insthync/dot-io-playfab-client)

## 1.17
- Upgrade to PUN2, Please read (https://suriyun-production.github.io/battle-io-docs/#/pages/101-update-to-pun2.md)

## 1.16
- Add skill system

## 1.15
- Reduce packets size
- Add custom equipment

## 1.14
- Add spawn position settings for specific team setting to `GameplayManager`
- Add `MonsterSpawnArea` developer can use it to spawn monsters when start the server

## 1.13
- Add password for room creation
- Fix invalid map name in waiting room UI
- Switch master client when watch Ads

## 1.12e
- Fix bots pickup currencies to players bugs
- Move map list and game rules from `Create game UI` to `Game instance`

## 1.12d
- Fix invalid asmdef locations

## 1.12c
- Add `Attack Signal Object` to Character Entity, can use this to show UIs which telling player that the character is attacking
- Fix clients play as spectator mode when host start game after created room

## 1.12b
- Fix missing button events
- Fix cannot play in offline mode
- Fix no bot in offline mode

## 1.12
- Add lobby system
- Add team death match mode
- Fix battle royale mode move outside safezone

## 1.11
- Add end match reward

## 1.10
- Can set start weapons at gameplay rules
- Not allow player attacks in Battle Royale mode when spawning

## 1.09
- Fix codes that duplicating with Fantasy Customization Pack project

## 1.08
- Add sendRate and sendRateOnSerialize options to SimplePhotonNetworkManager
- Fix empty bot player name

## 1.07
- Add the ability to dash, can set settings at Character Entity / Character Animator Controller

## 1.06
- Fix mobile controllers issues
- Add price option to In-Game Product

## 1.05
- Add monster entity, see Battle scene for example 
- When dead equip weapon will change to start equip weapon

## 1.04
- Fix disconnect errors
- Fix invalid random attack animation
- Remove unused files

## 1.03
- Add support idle animation changes by equip weapon
- Fix null exception errors when disconnect

## 1.02
- Fix missing room info in lobby list

## 1.01
- Add offline mode
- Fix bugs
