# LCVR Controller Profiles

This repo contains a list of input binding overrides that can be used to make different kind of controllers work correctly with the [Lethal Company VR mod](https://github.com/DaXcess/LCVR).

# Profiles

> These controller profiles are not provided by the developer of LCVR (except for the `default` profile), so it is not guaranteed that they work properly for every user

| Name                        | Author                                   | Comment                                                                                                                            |
| --------------------------- | ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `default`                   | [@DaXcess](https://github.com/DaXcess)   | These are the default controller bindings that are included with the LCVR mod                                                      |
| `leftgrip_sprint`           | @dzgreka                                 | This derivative of the default profile swaps the secondary use, and sprint button                                                  |
| `wmr`                       | @CH3k                                    | This just adds support for WMR remotes, jump is bound to right touchpad, Drop Item is bound to left touchpad                       |
| `index_touchpads`           | [@Bontebok](https://github.com/Bontebok) | For Index controllers, prevents joystick damage. Sprint left grip, crouch left touchpad, secondary right touchpad.                 |
| `htc_vive`                  | @KYRIS0                                  | This adds support for vive controller, jump is bound to left trigger                                                               |
| `crouch_switch`             | @LilBean64                               | This switches a couple controls, jump is secondary button, crouch is primary button, drop is joystick button, all right controller |
| `wmr_rebound_jump_and_drop` | @Collin8000                              | This switches two controls, jump is now bound to "A" and drop is bound to "B" Use with HP Reverb G2                                |
| `quest_ptt`                 | @Vrgamez                                 | Adds push to talk functionality for quest 3. Remaps in-game menu to left controller menu button and assigns ptt button to 'X'      |

# Applying a custom profile

In the mod's configuration, set the `ControllerBindingsOverrideProfile` option to the name of the profile binding you would like to use. This does however require an active internet connection, since these profiles are downloaded directly from this GitHub repository and will allow the use of new profiles without having to update the mod.

# Writing a custom profile

> This section is not yet finished

You can add a custom profile by either creating JSON files manually, or using the Unity Editor to create Input Action Assets, which you will have to export to a JSON file.

**Handy dandy resources**:

- [Unity XR Input](https://docs.unity3d.com/Manual/xr_input.html)
- [Input Common Usages](https://docs.unity3d.com/ScriptReference/XR.CommonUsages.html)

## Writing JSON manually

It is recommended to use the `default` profile as a baseline, which already contains valid input bindings in a valid format.

To change a binding: edit it's `path` key and change it to the binding of your choosing. If you know enough about Unity's Input System, you can also edit the `processors` key or use composites for more complex input binding (e.g. adding a binding that requires two inputs). Otherwise it is recommended to create these using an Input Action Asset inside of the Unity Editor.

## Using the Unity Editor

TODO

# Adding your profile

Fork this git repository, and add your variant of controller profiles.

Your controller profile should consist of two files: `lcvr_vr_inputs.json` and `lcvr_lc_inputs.json` (take a peek at the `default` profile to see how to set it up properly).

Place these inside of a directory with whatever name you want to give this profile. Please use lowercase names and replace spaces with underscores (`_`).

Next, add a README.md file to your profile that contains the list of keybinds. You can use the [README.md](default/README.md) from the `default` profile as a reference.

After you have done that, update **this** README.md file and add your profile to the list.

Once everything is ready, create a pull request, and if everything checks out, it will be merged.
