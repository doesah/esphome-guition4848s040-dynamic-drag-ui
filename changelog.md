### Firmware Changelog 

#### 1.1.24 Released on 2026.11.09
- Added a dithering algorithm for gradient background colors, ensuring smoother color transitions
- Fixed an issue where memory fragmentation after multiple updates occasionally caused automatic reboots
- Adjusted the backlight brightness range for a more uniform brightness adjustment

#### 1.1.23 Released on 2026.11.03
- Added full Chinese character set support (GB2312)
- Added Animation component

#### 1.1.22 Released on 2026.11.15
- Fixed touch point drift issues on certain devices

#### 1.1.21 Released on 2026.09.24
- Fixed layout calculation issues for the Segmented component

#### 1.1.20 Released on 2026.08.17
- Fixed origin offset issues during zooming

#### 1.1.19 Released on 2026.08.06
- Optimized event dispatching logic for Slider, Arc Controller, Segmented, and Switch components and improve performance and stability

#### 1.1.18 Released on 2026.08.05
- Optimized Slider and Arc Controller components to support custom value ranges
- Enhanced fonts and expanded the Chinese character set

#### 1.1.17 Released on 2026.08.04
- Upgraded time and date components to support fetching time from the Home Assistant server, allowing accurate time and date display in local networks without internet access
- Optimized event dispatching logic for Slider, Arc Controller, Segmented, and Switch components to reduce unnecessary HA communication and improve performance and stability

#### 1.1.16 (1-Gang Relay Version Only) Released on 2026.07.25
- Fixed an issue where changes in Action names caused blueprint templates to fail

#### 1.1.15 Released on 2026.07.25
- Fixed an issue where touching the screen could not wake it up after the backlight brightness was completely turned off

#### 1.1.14 Released on 2026.07.06
- Supported the `go_to_page` action to enable screen navigation to a designated page within Home Assistant
- Fixed a color flickering issue caused by transition animations being triggered in certain scenarios when button components are clicked

#### 1.1.13 Released on 2026.07.05
- Supported recolor for image components and background images

#### 1.1.12 Released on 2026.06.30
- Upgrade the slider component to better support curtain control scenarios.
  - Support both horizontal and vertical modes.
  - Support customizable slider sizes.
  - Support horizontal mirroring in horizontal mode.

#### 1.1.11 Released on 2026.06.27
- Fixed an issue where blueprint templates stopped working after changing device names in Home Assistant.
- Fixed an issue with persistent status styles.
- Added support for background images in styles to enable different background effects for different statuses.

#### 1.1.10 Released on  2026.06.25
 - Update Chinese Fonts and Optimize Common Character Sets

#### 1.1.9 Released on 2026.06.20
 - Fixed a value state synchronization issue with the switch component.

#### 1.1.8 Released on 2026.06.12
 - Optimized system menu
 - Fixed some known issues

#### 1.1.7 Released on 2026.06.06
 - Device system menu now supports English, Simplified Chinese, and Traditional Chinese, which can be configured in the interface settings
 - Supported custom bottom LOGO text

#### 1.1.6 Released on 2026.06.01
 - Fixed an issue where Wi-Fi was reset after each firmware upgrade (after updating to this version, Wi-Fi will not be reset during future firmware updates)

#### 1.1.5 Released on 2026.05.31
- Fixed several known issues

#### 1.1.4 Released on 2026.05.31
- Supported different Daylight Saving Time (DST) region settings for Time and Date components
- Added new date formats to the Date component: 01/31/2026 | January 31, 2026 | Jan 31, 2026 | Jan 31
- Improved long-term standby stability of the device

#### 1.1.3 Released on 2026.05.26
- Added a Segmented Control component, supporting local data binding

#### 1.1.2 Released on 2026.05.20
- Updated Chinese fonts, supporting Hong Kong Traditional and Taiwan Traditional Chinese
- Fixed several known issues

#### 1.1.1 Released on 2026.05.19
- Supported Traditional Chinese
- Added 3 new fonts for numbers and dates, providing more aesthetic font choices for screensavers, dashboards, and other scenarios

#### 1.1.0 Released on 2026.05.18
- Added an Arc Control component, suitable for building various dashboard scenarios
- Added local binding for Slider and Arc Control components, allowing real-time data output to text and other settable components for local linkage within the device

<details>
<summary>Earlier Logs</summary>
<content>

#### 1.0.10 Released on 2026.05.12
- Added Home Assistant command tool

#### 1.0.9 Released on 2026.05.10
- Added defense logic for unreasonable slider steps and ranges to avoid crashes

#### 1.0.8 Released on 2026.05.06
- Optimized image rendering to render at original size when width and height are not set

#### 1.0.7 Released on 2026.05.04
- Resolved an issue where JPG images failed to display when scaled
- Supported opacity style attributes for components

#### 1.0.6 Released on 2026.05.03
- Optimized image rendering in Image Map and Button components to ensure full images are displayed

#### 1.0.5 Released on 2026.05.02
- Fixed crash issues caused by certain extreme style values

#### 1.0.4 Released on 2026.04.24
- Supported precision and step settings for the Slider component

#### 1.0.3 Released on 2026.04.20
- Fixed an issue where operating the Switch component did not trigger Value Change state changes

#### 1.0.2 Released on 2026.04.19
- Fixed an issue where too many component styles caused the interface to fail to display after updating

#### 1.0.1 Released on 2026.04.16
- Supported style attribute: Text Alignment

#### 1.0.0 Released on 2026.03.19
- Initial release
</content>
</details>