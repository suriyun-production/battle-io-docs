# Changelog (LiteNetLibManager)
**I decided to make all important parts to be an open source projects, so you won't have to buy this one, you can find source codes [here](https://github.com/insthync?tab=repositories&q=io-core&type=&language=&sort=)**

## 1.74 (2022-07-04)
- Update Purchasing integration.
- Update Facebook SDK integration.
- Update Google Play Games Service integration.
- Update PlayFab SDK integration.
- Setup events to update purchased items (You won't have to set it by yourself anymore).
- Change demo's currency ID from `GOLD` to `GO` to make it compatible with PlayFab.

## 1.73b (2022-02-26)
- Update to Unity version 2020.3.26f1.
- Fix score and kills not being counted properly.

## 1.73 (2021-10-22)
- Fix character cannot being pushed by forces.
- Fix character cannot change weapon by attributes.
- Fix status effects not being applied properly.
- Fix Playfab data exporter not export bundles.

## 1.72 (2021-08-07)
- Reduce packet size.
- Add blocking action.

## 1.71b (2021-04-05)
- Fix null data break update loop.
- Fix unsynced aim position.
- Don't update aim position for non-owning characters.

## 1.71 (2021-03-29)
- Improve character movement, now it has to attached `CharacterMovement` component to `CharacterEntity` when you attaches `CharacterMovement` component, you have to set `CharacterController` settings to cover your character and you have to set attached colliders to be trigger collider.
- Add third person view mode, you have to change `FollowCamera` component which usaully attached to main camera to `FollowCameraControls` component.
- Add `ViewMode` settings to `CharacterEntity`, you can set it to `TopDown` and `ThirdPerson`.
- Add `TopDownViewModeSettings` it will be applied to `FollowCameraControls` and main camera when `ViewMode` is `TopDown`.
- Add `ThirdPersionViewModeSettings` it will be applied to `FollowCameraControls` and main camera when `ViewMode` is `ThirdPerson`.

## 1.70c (2021-02-21)
- Update to latest LiteNetLibManager version.
- Fix networked prefabs not registered before server start.
- Add `-gameBotCount` environment configuration, use it to set bot count when start dedicated server.
- Add `-gameMatchTime` environment configuration, use it to set match time when start dedicated server.
- Add `-gameMatchKill` environment configuration, use it to set kill count to win when start dedicated server.
- Add `-gameMatchScore` environment configuration, use it to score count to win when start dedicated server.
- Kick client whom connecting while match ended.
- Restart server after match ended.
- Fix wrong player's ranking when match end.
- Fix null-reference for on-screen mobile controller when start non-mobile games.

## 1.70 (2020-07-02)
- Change networking system to `LiteNetLibManager` (You should read [how to update](../pages/104-update-to-litenetlib.md)).
- Change to move characters by changes transform's position, rigibody will be used to applies force.
- Add `ExplosionForce` and `ExplosionForceRadius` settings to `Damage Entity` it will applies to force character when damage entity hit or explode.
- Add `DivideSpreadedDamageAmount` if this is `TRUE`, damage amount will be divided by amount of spread damages.

# Changelog (UNET)

## 1.61 (2020-02-12)
- Add `StatusEffectEntity` which can set to `DamageEntity` or `SkillData` as a buffs or nerfs to increase or decrease character's stats.
- Fix null exceptions occuring after enter or exit `HideArea`

## 1.60
- Fix invalid weapon model's damage launch transform position.
- Implement NavMesh to BotEntity, Bot will find paths from NavMesh if there is baked NavMesh in the scene. Developers don't have to add NavMeshAgent to BotEntity.
- Bots can dash.
- Bots can use skills
- Bots can increase their attributes.

## 1.59b
- Fix hide area bugs

## 1.59
- Add `HideArea`, developer can attach this component to grasses which will be used to hide characters

## 1.58d
- Avoid null exception when there is no head to select
- Add plane to Battle Royale demo

## 1.58c
- Fix invalid execute order

## 1.58b
- Fix bought items won't be saved

## 1.58
- Add codes to support Playfab integration project (https://github.com/insthync/dot-io-playfab-client)

## 1.57
- Add skill system

## 1.56
- Reduce packets size
- Add custom equipment

## 1.55b
- Fix bots pickup currencies to players bugs
- Move map list and game rules from `Create game UI` to `Game instance`
- Add `Attack Signal Object` to Character Entity, can use this to show UIs which telling player that the character is attacking

## 1.55
- Add end match reward

## 1.54
- Can set start weapons at gameplay rules
- Not allow player attacks in Battle Royale mode when spawning

## 1.53
- Fix codes that duplicating with Fantasy Customization Pack project

## 1.52
- Add the ability to dash, can set settings at Character Entity / Character Animator Controller

## 1.51
- Fix mobile controllers issues
- Add price option to In-Game Product

## 1.50
- Add monster entity, see Battle scene for example
- When dead equip weapon will change to start equip weapon

## 1.49
- Fix disconnect errors
- Fix invalid random attack animation
- Remove unused files

## 1.48
- Add support idle animation changes by equip weapon

## 1.47
- Add kill notify messages
- Fix battle royale mode not work on Master Server Framework integration
- Fix jump input not work sometime

## 1.45
- Improve performance by reduce amount of attack messages
- Add is hidding in character entity, use it to set character hide state

## 1.44
- Fix damage not calculate on dedicate server

## 1.43
- Add battle royale game mode

## 1.42
- Add chat and emoticon

## 1.41
- Add reward currency when kill other characters

## 1.40
- Add deathmatch game mode

## 1.39
- Make UIGameplay instantiating by Game rules
- Make character can jump (Try space bar butt)
- Add command line settings for dedication
- Can set to show mobile joystick or not via GameInstance (Home scene)
- Score/Kill/Dead reset immediately when dies

## 1.38
- Fix random animation bugs
- Add network game framework to prepare future game modes
- Add more secure monetization save

## 1.35
- Make character gravity supports so characters can walks on slopes
- Add trap entity

## 1.34
- Fix invalid damage entity transform at clients
- Improve damage spread
- Fix damage entity effects does not plays at clients some time
- Fix damage entity does not disable renderer at clients when hit objects
- Fix power up entity effects does not plays at client some time

## 1.33
- Add more properties to customize bots
- Add black fade
- Add audio manager
- Improve networking performance

## 1.32
- Add invincible status, will be activated when spawn
- Add spread damages status
- Add change weapon with attributes / powerup

## 1.31
- Improve graphics
- Fix bugs

## 1.30
- Randomize character attributes
- Multiple attacke animation
- Fix bugs

## 1.25
- Fix bugs
- Improve Network Discovery to show scene and player count
- Improve Ads monetize, now it's able to set random-able rewards
- Improve IAP products, now it's able to set more than 1 currencies

## 1.20
- Add watch ads to receives gold
- Add watch ads to respawn without reset stats

## 1.10
- Fix Bugs
- Improve Damage Entity
- Add Bots System
- Add IAP
- Add Selling Items
- Add Item Attributes
