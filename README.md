# BrezNET-iOS
Home Assistant theme based on Apple iOS colours.

Main Dark
![](https://github.com/brezlord/BrezNET-iOS/blob/main/docs/main-dark.png)

Lights Dark
![](https://github.com/brezlord/BrezNET-iOS/blob/main/docs/lights-dark.png)

Main Light
![](https://github.com/brezlord/BrezNET-iOS/blob/main/docs/main-light.png)

Lights Light
![](https://github.com/brezlord/BrezNET-iOS/blob/main/docs/lights-light.png)

Created by [BrezLord](https://github.com/brezlord) for Home Assistant
This theme has been designed to work on Samsung Galaxy Tab A (2019, 10.1") [SM-T510] as a wall mounted display for Home Assistant. The theme displays equally as good on mobile devices.

The theme is based on Apple Colors from - (https://developer.apple.com/design/human-interface-guidelines/color)
Clolor palette used iOS, iPadOS and system grey colors.

I plan on continuing to develop and improve this theme.

# Installation

## HACS Installation

Search for BrezNET iOS theme within the community store & Install

You need to have a themes folder in order to install this theme.

1. Go to your configuration.yaml file and add the following 

```
frontend:
  themes: !include_dir_merge_named themes
``` 

## Manual Installation

1. Download the themes folder from this repo
2. Unzip the contents and extract the themes folder into Home Assistant's root folder.
 - The above assumes you don't already have a themes folder, **if you do read below!**
 - If you already have a themes folder, then just extract the BrezNET iOS Theme folder into root/themes/
3. Make sure the following is in your configuration.yaml folder

```
frontend: 
  themes: !include_dir_merge_named themes
```
4. Restart your Home Assistant server
5. Select the BrezNET iOS theme in your user profile settings, don't forget to set the mode.

## Automate theme

If you would like to automate your theme so it is always the BrezNET iOS Theme across any device, you can do this via an automation.

1. Click on configuration
2. Click on Automations
3. Click + Create Automation
4. Click   Create new automation - Start with an empty Automation"
5. Click + Add Trigger
- In the search box type 'home' select 'Home Assistant - When Home Assistant starts up or shuts down'
- Select the start option

![](https://github.com/brezlord/BrezNET-iOS/blob/main/docs/add_trigger.png)

6. Scroll down to Then do, click + Add Action
- In the search box type 'theme' select 'Home Assistant Frontend: Set the default theme'
- Service: Home Assistant Frontend: Set the default theme
- Theme: BrezNET iOS
- Tick Mode and select either Dark or Light

![](https://github.com/brezlord/BrezNET-iOS/blob/main/docs/add_action.png)

![](https://github.com/brezlord/BrezNET-iOS/blob/main/docs/automation.png)

7. Click on save and change the name to "Theme - Set Default Theme"
