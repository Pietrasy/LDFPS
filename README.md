# LDFPS
A prototype FPS Shooter created entirely in blueprints. The project demonstrates: <br />
- Shooting mechanic with consideration of recoil and bullet spread
- Multiple fire modes: Full, Burst, Single
- An Inventory system for switching between weapons and saving their state
- Weapon pickups that allow the player to collect or swap waepons
- HUD elements showing ammo count and inventory status
- A hitmarker that appears on a successful projectile hits
- A multiplayer-oriented level design created for team deathmach, designed with attention to gameplay flow, spawn points, primary and secondary routes, and combat zones
- Hittable targets and explosive barrels!

### Table of Content:
[General Overview](#General-Overview)<br/>
[Controls](#Controls)<br/>
[Creating a new weapon](#Creating-a-new-weapon)<br/>
[Setting up a spawner](#Setting-up-a-spawner)<br/>
[Picking up or swapping a weapon](#Pick-up-or-exchange-a-weapon)<br/>
[Level Design Document](https://drive.google.com/file/d/1lckq297p5YfapVDh-aDoTaedepVvHP1Z/view?usp=sharing)<br/>

## General Overview
The player can pick up weapons that belong to one of three categories: Main, Secondary, or Special. Once picked up, the weapon is assigned to the appropriate slot and displayed in the inventory widget.<br/><br/>
Weapons feature different fire modes: single, burst, and full-auto. Firing is affected by recoil and bullet spread. The player can switch between equipped weapons. If the player picks up a weapon of a type already present in their inventory, it replaces the one currently stored in that slot.<br/><br/>
Weapon pickups display information in the component widgets.<br/>
Hit feedback is provided via a hitmarker on successful shots.<br/>
The environment includes interactive elements such as explosive barrels and reactive targets.<br/>

https://github.com/user-attachments/assets/3470c5ff-a6f5-41f2-bdb8-230b9c35dcc8


Weapon showcase: Rifle, Shotgun, Sniper, Rail Bolt, SMG, and Machine Gun.<br/>

https://github.com/user-attachments/assets/a43fabde-23e0-487d-bad9-ddb1a29a0635





## Controls
- **Left Mouse Button** - Fire<br />
- **Scroll Wheel** - Switch to the next or previous weapon<br />
- **R** - Reload<br />
- **E** - Interact<br />
- **Space** - Jump<br />
- **Left Shift** - Sprint<br />
- **1** - Equip a main weapon<br />
- **2** - Equip a secondary weapon<br />
- **3** - Equip a special weapon<br />
- **Tab** - Toggle the tutorial panel<br />

## Creating a new weapon
Create a data asset that inherits from **PDA_WeaponData**.<br/>
![CreatingWeaponDataAsset](https://github.com/user-attachments/assets/fb3b5879-4aad-4918-a771-5a0bed57feaf)
<br/>Set the details of weapon in data asset.<br/>
![DetailsToSettingUpWeapon](https://github.com/user-attachments/assets/eb4678a4-bc93-4d42-bcdb-18bbd50d6c47)

## Setting up a spawner
To spawn a weapon, place a **BP_WeaponSpawner** in the level and assign the **Weapon to Spawn** parameter.<br/>
![SettingUpWeaponPickup](https://github.com/user-attachments/assets/a2fff95d-de98-4ce9-80b3-b4d14b5dc7d3)

## Pick up or exchange a weapon
When a weapon spawns, a widget appears displaying information about it.
![ScreenShot00001](https://github.com/user-attachments/assets/d3fb5435-3c20-4690-a8e5-34c94be320e6)
If the player's inventory already contains a weapon of the same `weapon type` as the on in the spawner (both Rail Gun and Rifle are `main` type), the two will be swapped.
![ScreenShot00005](https://github.com/user-attachments/assets/50aa9dd1-2969-42b4-9ecb-093c46665f18)
![ScreenShot00006](https://github.com/user-attachments/assets/efedb94f-d83f-4e6c-89c4-45ce2ef62780)

## [Level Design Document)](https://drive.google.com/file/d/1lckq297p5YfapVDh-aDoTaedepVvHP1Z/view?usp=sharing)
![ScreenShot00002](https://github.com/user-attachments/assets/3c6d38b7-5210-4cbb-b1eb-e3de9419af4e)

