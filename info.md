<h1>BrezNET-iOS</h1>
<p>
	<a href="https://github.com/brezlord/BrezNET-iOS/stargazers"><img src="https://img.shields.io/github/stars/brezlord/BrezNET-iOS?colorA=363a4f&colorB=ffc300&style=for-the-badge"></a>
	<a href="https://github.com/brezlord/BrezNET-iOS/issues"><img src="https://img.shields.io/github/issues/brezlord/BrezNET-iOS?colorA=363a4f&colorB=f5a97f&style=for-the-badge"></a>
	<a href="https://github.com/brezlord/BrezNET-iOS/pulls"><img src="https://img.shields.io/github/issues-pr/brezlord/BrezNET-iOS?colorA=363a4f&colorB=a6da95&style=for-the-badge"></a>
</p>

# Home Assistant theme based on Apple iOS colours

<p align="center">
	<img src="https://raw.githubusercontent.com/brezlord/BrezNET-iOS/main/docs/main-dark.png"/>
</p>

## Previews

<details>
<summary>🌚Dark</summary>
<img src="https://raw.githubusercontent.com/brezlord/BrezNET-iOS/main/docs/main-dark.png"/>
<img src="https://raw.githubusercontent.com/brezlord/BrezNET-iOS/main/docs/lights-dark.png"/>
</details>
<details>
<summary>🌞Light</summary>
<img src="https://raw.githubusercontent.com/brezlord/BrezNET-iOS/main/docs/main-light.png"/>
<img src="https://raw.githubusercontent.com/brezlord/BrezNET-iOS/main/docs/lights-light.png"/>
</details>

Created by [BrezLord](https://github.com/brezlord) for Home Assistant.

This theme has been designed to work on the Samsung Galaxy Tab A (2019, 10.1") [SM-T510] as a wall mounted display for Home Assistant. The theme displays equally as good on mobile devices.

The theme is based on Apple Colors from - https://developer.apple.com/design/human-interface-guidelines/color

Clolor palette used iOS, iPadOS and system grey colors.

The following addons were used in addition to the built in cards to create the below examples.
- [Button Card](https://github.com/custom-cards/button-card)
- [Fan Control Entity Row](https://github.com/finity69x2/fan-control-entity-row)
- [Atomic Calendar Revive](https://github.com/totaldebug/atomic-calendar-revive)
- [Clock Weather Card](https://github.com/pkissling/clock-weather-card)
- [Platinum Weather Card](https://github.com/Makin-Things/platinum-weather-card)
- [Layout-card](https://github.com/thomasloven/lovelace-layout-card)
- [Frigate Home Assistant Integration](https://github.com/blakeblackshear/frigate-hass-integration)

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
2. Unzip the contents and copy the themes directory into config/ or root directory if running Home Assistant core in Docker.
 - The above assumes you don't already have a themes folder, **if you do read below!**
 - If you already have a themes folder, then just extract the BrezNET-iOS folder into config/themes/
3. Make sure the following is in your configuration.yaml file:

```
frontend: 
  themes: !include_dir_merge_named themes
```
4. Restart your Home Assistant server
5. Select the theme in your user profile settings

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
