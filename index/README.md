# Valve Index Controller Profile

## LC Controls

|      Action      | PC               | VR                | Notes                                                             |
| :--------------: | ---------------- | ----------------- | ----------------------------------------------------------------- |
|       Look       | Mouse Movement   | HMD               | Will use right joystick X for snap-turning                        |
|       Move       | WASD, Arrow Keys | Left Joystick     |                                                                   |
|       Jump       | Space            | A                 |                                                                   |
|      Sprint      | Shift            | (Disabled)        | Taken over by the mod, check `VR Inputs` below                    |
|     OpenMenu     | Escape, Tab      | X                 |                                                                   |
|     Interact     | E                | (Disabled)        | Taken over by the mod, check `VR Inputs` below                    |
|      Crouch      | Ctrl             | R Joystick Button |                                                                   |
|       Use        | LMB              | Right trigger     |                                                                   |
|   ActivateItem   | LMB              | Right trigger     |                                                                   |
|     Discard      | G                | B                 |                                                                   |
|    SwitchItem    | ScrollY          | Right joystick Y  |                                                                   |
| ItemSecondaryUse | Q                | L Grip Button     |                                                                   |
| ItemTertiaryUse  | E                | R Grip Button     |                                                                   |
|     PingScan     | RMB              | Left Trigger      |                                                                   |
|    BuildMode     | B                | L Grip + R Grip   | Press both buttons simultaneously to go into build mode           |
|      Delete      | X                | B                 |                                                                   |
|  QEItemInteract  | Q, E             | (Disabled)        | Depricated since V45, Use secondary and tertiary use instead      |
|    EnableChat    | Slash            | (Disabled)        | Chat is just not something we want to do in VR                    |
|    SubmitChat    | Enter            | (Disabled)        | Chat is just not something we want to do in VR                    |
| ReloadBatteries  | R                | (Disabled)        | Building mode prop rotating. In VR this uses Pivot in `VR Inputs` |
|   InspectItem    | Z                | (Disabled)        | Only for clipboard, disabled because there's more important stuff |
|   VoiceButton    | T                | (Disabled)        | IDK arbitary push to talk is not very favorable in VR             |
|      Emote1      | 1                | (Disabled)        | Will not bother adding this into VR                               |
|      Emote2      | 2                | (Disabled)        | Will not bother adding this into VR                               |
| ConfirmBuildMode | V                | (Disabled)        | Unused in the base game                                           |
|  SetFreeCamera   | C                | (Disabled)        | Most likely a developer only cheat                                |
|    SpeedCheat    | H                | (Disabled)        | Most likely a developer only cheat                                |

## VR Controls

|    Action    | Bind              | Notes                                                                                   |
| :----------: | ----------------- | --------------------------------------------------------------------------------------- |
| Reset Height | Y                 | Recalculates the offset between your headset and the floor                              |
|     Grab     | R Grip Button     | The grab and interact button for world interactables                                    |
|     Turn     | R Joystick X Axis | If you have snap/smooth turning enabled, this will determine the direction to rotate in |
|    Pivot     | R Joystick        | Spectator camera pivoting and build mode prop rotating                                  |
|    Sprint    | L Joystick Button | Must either be held down or toggles based on the configuration that is used             |

## Diff with `default`

> Last updated: **22 Jan 2024**

`$ diff -u default/profile.inputactions index/profile.inputactions`
```diff
--- default/profile.inputactions        2024-01-22 18:40:34.850776800 +0100
+++ index/profile.inputactions  2024-01-22 22:41:27.613311500 +0100
@@ -297,7 +297,7 @@
                 {
                     "name": "Use: Right Trigger",
                     "id": "6527e10c-1acf-410f-b439-7e2db96bf25d",
-                    "path": "<XRController>{RightHand}/triggerButton",
+                    "path": "<XRController>{RightHand}/trigger",
                     "interactions": "",
                     "processors": "",
                     "groups": "",
@@ -308,7 +308,7 @@
                 {
                     "name": "Activate Item: Right Trigger",
                     "id": "6d80dd41-4bf1-4581-bf98-839b02e7219b",
-                    "path": "<XRController>{RightHand}/triggerButton",
+                    "path": "<XRController>{RightHand}/trigger",
                     "interactions": "",
                     "processors": "",
                     "groups": "",
```
