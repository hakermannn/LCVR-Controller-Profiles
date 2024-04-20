# LCVR Controller Profiles

This repo contains a list of input binding overrides that can be used to make different kind of controllers work correctly with the [Lethal Company VR mod](https://github.com/DaXcess/LCVR).

# Profiles

> These controller profiles are not provided by the developer of LCVR (except for the `default` profile), so it is not guaranteed that they work properly for every user

| Name                        | Author(s)                                                       | Comment                                                                                                                                                         |
| --------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ✨ `default`                | [@DaXcess](https://github.com/DaXcess)                          | These are the default controller bindings that are included with the LCVR mod                                                                                   |
| ✨ `index`                  | [@Phil25](https://github.com/Phil25)                            | Default controller bindings with Index-specific right trigger                                                                                                   |
| ✨ `htc_vive`               | @KYRIS0                                                         | This adds support for vive controller, jump is bound to left trigger                                                                                            |
| ✨ `reverb_g2`              | @Collin8000, @danielallencoates                                 | Adds support fot the HP Reverb G2 controllers by rebinding several functions to A, B, X, and Y                                                                  |
| ✨ `wmr`                    | @danielallencoates                                              | Adds support for WMR remotes via Generic XR Input Bindings                                                                                                      |
| ❗`index_damage_prevention`   | [@PieMonsterEater](https://github.com/PieMonsterEater)          | Prevents joystick damage on index controllers. Crouch Left Touchpad, Sprint Right Touchpad. Otherwise same as index profile.                                    |
| ❗`wmr_direct_inputs`         | @danielallencoates                                              | Adds support for WMR remotes via WMR's Direct bindings                                                                                                          |
| ❗`index_gripforce`           | @QuietFlair                                                     | This makes it so you have to grip hard to interact with things. Probably only works if you are using the Knuckles                                               |
| ❗`crouch_switch`             | [@LilBean64](https://github.com/LilBean64)                      | This switches a couple controls, jump is secondary button, crouch is primary button, drop is joystick button, all right controller. Also adds binds for emotes. |
| ❗`default_emotes`            | [@LilBean64](https://github.com/LilBean64)                      | This is basically just the default controls with emote bindings. Menu is the menu button on the left controller                                                 |
| ❗`joystick_jump`             | @hmcl9                                                          | This binds jumping to the right joystick Y-axis, and moves item swapping to A and B for forwards and backwards respectively                                     |
| ❗`htc_vive_alt`              | [@FloofyBoof](https://github.com/FloofyBoof)                    | Uses tap and hold inputs to combine multiple actions to the same button. (e.g. Ping and Open Menu share the left menu button)                                   |
| ❗`leftgrip_sprint`           | @dzgreka                                                        | This derivative of the default profile swaps the secondary use, and sprint button                                                                               |
| ❗`index_touchpads`           | [@Bontebok](https://github.com/Bontebok) (pre 1.1.0), @Coomquat | For Index controllers, prevents joystick damage. Sprint left grip, crouch left touchpad, secondary right touchpad.                                              |
| ❗`index_lefthanded_movement` | @EnrageKoala                                                    | Index controllers, switched movement and turning actions between left and right.                                                                                |
| ❗`wmr_gripsprint_joystickdrop` | @UnityMakesWorlds                                             | wmr controllers, switched sprint to grip and drop item to left stick click.                                                                                     |
| ❗`leftstick_only`            | [@hakermannn](https://github.com/hakermannn)                    | ONLY WORKS ON QUEST rebinds Y to menu, hold y to make leftstick act like base rightstick                                                                        |

> Profiles with an `✨` emoji are built into the mod itself and don't need to be explicitly set in the config

> Profiles with an `❗` emoji may not support physical interactions using the left hand

# Applying a custom profile

In the mod's configuration, set the `ControllerBindingsOverrideProfile` option to the name of the profile binding you would like to use. This does however require an active internet connection, since these profiles are downloaded directly from this GitHub repository and will allow the use of new profiles without having to update the mod.

# Writing a custom profile

You can add a custom profile by either using the Unity Editor to create Input Action Assets, which you will have to export to a file to be uploaded to this repo.

**Handy dandy resources**:

- [Unity XR Input](https://docs.unity3d.com/Manual/xr_input.html)
- [Input Common Usages](https://docs.unity3d.com/ScriptReference/XR.CommonUsages.html)

## Using the Unity Editor

To be able to use the Unity Editor, you must first have it installed. The Unity version that this game uses is **Unity 2022.3.9f1**, however it should not matter which version of Unity you are using.

To start, create a new Unity project. You can use any project template you like, it doesn't specifically have to be 3D.
![image](https://github.com/DaXcess/LCVR-Controller-Profiles/assets/46288749/38212fa3-61b4-49a6-874e-d75e4bbf03fb)

Give your project a name like "LCVR-Inputs". It doesn't really matter what you call it.
![image](https://github.com/DaXcess/LCVR-Controller-Profiles/assets/46288749/fc4db25e-644a-4b8b-b94f-1fb63be446c6)

Next up you will have to install Unity's Input System. To do that, go to the Package Manager, make sure you are in the Unity Regisistry, and install the "Input System" package.

![image](https://github.com/DaXcess/LCVR-Controller-Profiles/assets/46288749/db382355-c6d2-4d63-887a-9da31df5fe33)
![image](https://github.com/DaXcess/LCVR-Controller-Profiles/assets/46288749/57e83d15-463a-42ce-aa01-2ae408226045)

If you receive a warning that you have to restart your editor, press Yes.

![image](https://github.com/DaXcess/LCVR-Controller-Profiles/assets/46288749/55938e58-ebae-4f07-81f0-2992b62eb5dd)

Now that you have restarted your editor, you can go ahead and tinker with input actions. The easiest way to get started is by downloading the `profile.inputactions` file from the `default` directory in this repo, and dropping it inside your Unity editor. From here you can double click the Input Action Asset, and you will get a screen where you can see and edit the controller bindings.

![image](https://github.com/DaXcess/LCVR-Controller-Profiles/assets/46288749/05defe20-ed4d-4edc-8f62-e4ac0fb9e8c6)

Keep in mind that when editing, you must not add/remove/rename any Action Maps and Actions, since that will most likely break the mod and the game. Modifying them is fine though (changing properties on the actions). The bindings can be freely deleted/added/modified to your hearts content, just make sure that the game is playable with them ;)

The **Movement** action map is an actual copy of the actions that Lethal Company uses internally. The bindings in here will directly replace the bindings in the game. Some bindings (currently `Sprint` and `Interact`) should not get bindings, as they have been taken over by the mod. Make use of the **Controls** action map instead, which the mod uses internally.

# Adding your profile

Fork this git repository, and add your variant of controller profiles.

Your controller profile should consist of two files: `profile.inputactions` and `README.md` (take a peek at the `default` profile to see how to set it up properly).

Place these inside of a directory with whatever name you want to give this profile. Please use lowercase names and replace spaces with underscores (`_`).

Next, add a README.md file to your profile that contains the list of keybinds. You can use the [README.md](default/README.md) from the `default` profile as a reference.

After you have done that, update **this** [README.md](README.md) file and add your profile to the list.

Once everything is ready, create a pull request, and if everything checks out, it will be merged.
