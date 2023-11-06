## How to remap Steam/QAM Buttons to Scrollwheel (OLD)

### Introduction
This guide will show you how to install Input Remapper and how to remap your scrollwheel to act as your Steam Menu/Quick Access Menu toggles. Please note that this is ***NOT a permanant solution***. You should try to install HandyGCCS (handycon) before attempting this. But if no other fixes are working for you, this workaround will at least get bare minimum functionality, with some quirks.

### Quirks
- A 2nd controller will appear in the Steam Settings>Controller area
- When resuming from sleep in some games, the game with attach to this 2nd controller instead of the built in one, forcing you to restart the game

### Step 1

first you'll need to install input-remapper from the AUR

```pikaur -S input-remapper-git```
```sudo systemctl restart input-remapper```
```sudo systemctl enable input-remapper```

### Step 2

Launch the application, and remap the scroll up and down functions to the following

```BTN_MODE``` (for the Steam Menu)
```BTN_MODE+BTN_A``` (for the Quick Access Menu)

This should provide limited functionality of the Steam and Quick Access Menu buttons until you can get another solution running.
