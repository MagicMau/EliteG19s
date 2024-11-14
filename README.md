# EliteG19s Manual

##### version 3.7

Welcome and thank you for using my companion app for Elite Dangerous!

As I am building this app, more and more functionality is included.
I try to make as much of it optional, so that you do not feel
forced to use it. This does mean however that lots of functionality
is hidden in options, settings and secret key combinations.

The purpose of this manual is to shine some light on all the possibilities
the EliteG19s companion app offers.

([Click here if you have trouble running the app after upgrading](#AppWillNotStartAfterUpgrade))

## Contents

1. [FAQ](#FAQ)
2. [Installation](#Installation)
   1. [Previous Version](#PreviousVersions)
3. [Controls](#Controls)
   1. [Keyboard Controls](#Keyboard)
   2. [Mouse Controls](#Mouse)
   3. [VoiceAttack](#VoiceAttack)
   4. [Hotkeys](#Hotkeys)
   5. [Orrery View](#Orrery)
   6. [GPS View](#GPS)
   7. [Philips Hue](#Hue)
   8. [Lua Scripting Support](#Lua)
4. [Options File](#Options)
   1. [Editing Radio Stations](#RadioStations)
   2. [Editing Youtube Channels](#TVStations)
   3. [Editing Spotify Playlists](#SpotifyPlaylists)
   4. [Editing Websites](#Websites)
5. [Windows 10 Additional Voices](#MoreVoices)
6. [Troubleshooting](#Troubleshooting)
7. [Contact](#Contact)

## <a name="FAQ"></a>FAQ

**Q: What does this app offer me?**<br>
A: a lot!

- Information on your current location in game
- Space Traffic Control
- Text-To-Speech for messages from NPCs and other CMDRs
- Orrery view of the system you are currently in
- Radio player for Elite themed internet radio ([Radio Skvortsov](http://radio.entropy101.com/), [Radio Sidewinder](http://www.radiosidewinder.com) and many more, and you can add your own!)
- Control Spotify (only for Spotify Premium subscribers)
- Use Philips Hue to display light effects
- News ticker for GalNet news, r/EliteDangerous
- Music player for local files (all kinds of formats)
- GPS functionality when in your SRV or in orbital flight
- Watch YouTube videos
- Watch Twitch streams
- Upload flight log to [EDSM](https://www.edsm.net)
- Upload your commander's stats to [Inara](https://www.inara.cz)
- Upload latest trade data to [EDDN](https://eddb.io)
- Retrieve current information from [EDDB](https://eddb.io)
- Use the official Frontier Companion API to download latest trade data
- Convert screenshots to JPG, with metadata on location
- Audio visualizations
- [VoiceAttack](https://www.voiceattack.com) support
- Hotkey support (e.g. to map functionality to HOTAS buttons)
- Lua scripting support for additional customization

**Q: Is a Logitech keyboard required?**<br>
A: No! Although the app was originally created for use with a Logitech LCD keyboard,
this hasn't been a requirement for a long time. The app will happily display the
information on a regular window on your screen.

**Q: Does this work with Logitech Arx (second screen for mobile)?**<br>
A: Yes! If you have installed the latest
[Logitech Gaming Display software](http://support.logitech.com/en_us/software/lgs),
and have the Logitech Arx app on your phone or tablet, you can see the information
there as well.

**Q: Are there more voices available?**<br>
A: The app uses the SAPI5 Text-To-Speech voices that you have installed on your PC. There are excellent voices available for purchase, but if you have Windows 10 there are methods of installing additional voice packs to provide more voices. For more details check the section [Windows 10 Additional Voices](#MoreVoices).

**Q: Can I display this in my VR set?**<br>
A: Yes! Thanks to CMDR MacDaddyB who figured this out. Using a
[special piece of software](https://github.com/Hotrian/OpenVRDesktopDisplayPortal)
you can now position the EliteG19s window in your cockpit!
There is also a [reddit post on Oculus Dash](https://www.reddit.com/r/EliteDangerous/comments/7zwm3o/elite_in_vr_is_even_better_with_oculus_dash/) that may be of interest to you.

**Q: But I don't have a VR set, can I still display it in my cockpit?**<br>
A: You sure can! Try [OnTopReplica](http://ontopreplica.codeplex.com/).

**Q: Do you store my account information?**<br>
A: Only if you decide so to facilitate linking to external services.
All information is securely stored on _your_ harddrive and is _never_ sent to other destinations than the intended one.<br>
Also, the information is heavily encrypted when it is stored in the Windows Credential Manager to prevent anyone to be able to retrieve your password from the app.

**Q: Can I open multiple windows?**<br>
A: Yes! In the Windows system tray (next to the clock) you will find the EliteG19s icon. Right clicking this gives you the option to open a new window.
You can have as many as you like. As from version 3.1 the app can remember open windows and reopen them when you restart the app.

**Q: Do I need a Spotify Premium account?**<br>
A: Only for the Spotify bits!

**Q: Why does the orrery view not match up with the in game position of planets?**<br>
A: Simply because planets do not move fast enough to make pretty animations! I like the
idea of an orrery that moves around. That's why in the orrery view one real second equals to one Earth day by default. But, using the buttons on screen you can control time and make it as quick or slow as you want.

**Q: The orrery is not correct! How come?**<br>
A: Unfortunately, not all information that's available in the game's Stellar Forge is available for third party apps. That means that the algorithms I have created make some assumptions, and do quite a bit of the physics calculations themselves to approximate the in-game results.
For instance, one of the things I simply don't know is how the planets are positioned relative to each other at any given time. But, as there is time compression in effect anyway, that does not really matter. :)<br>
If you notice systems where the orrery is way off, please let me know!

**Q: Why can't I find my POIs in the GPS view?**<br>
A: Because there are so many planets in the game and thus potentially many different
Points of Interest, the app only lists the POIs that are on the planet that you fly over,
or have landed on.<br>
To make it somewhat easier to find what you are looking for, when you are not a planet,
the POI list will show the list of POIs for the current system, sorted per planet.

**Q: Why doesn't the GPS know about all those in game locations, such as INRA bases?**<br>
A: I keep a manually curated list of waypoints that you can download through the GPS, simply choose the option "Download Public POIs". I try to keep this up to date to the in game discoveries. However, if you find I have missed one, please let me know so that others can find it too!

**Q: I want to buy you a cup of coffee, what's your Paypal link?**<br>
A: https://paypal.me/MagicMau

## <a name="Installation"></a>Installation

Installation is easy, you can simply click [this link to install
and run the app](https://apps.magicmau.nl/EliteG19s/EliteG19s-latest.msi).

Often when you download and start this file, Windows Smartscreen will warn you about unverified sources. This is because I have not digitally signed the app with an official developer's certificate. Feel free to click 'Run anyway'.

The installer itself will also help you provide the necessary details to log in to the Frontier API, EDSM, Inara and Elite Galaxy Online where applicable. If you choose to opt out here, you can always opt back in by going through the options screens of the app.

### <a name="PreviousVersions"></a>Previous Versions

If for some reason the current version gives you errors, please make sure that you let me know. If I don't know about the issue, I can't fix it! Download the previous version by clicking on [this link](https://apps.magicmau.nl/EliteG19s/EliteG19s-3.1.3.msi). Please make sure that you have uninstalled any existing versions of EliteG19s before installing an older version.
Also, I cannot guarantee that all your settings can be restored when downgrading, but most should still work.

## <a name="Controls"></a>Controls

If you have a Logitech LCD keyboard you can use the corresponding buttons to control the app.
If you do not have such a keyboard and display a regular window you can use the mouse and keyboard to control the app.
Using voice commands (through VoiceAttack) or hotkeys, you can control the app as well.

### Tray icon

When you start the app you will see its icon in the system tray, next to the clock and volume icons. Right clicking the icon gives you options to open a new window, in a different size, or exit the app.

### <a name="Keyboard"></a>Keyboard controls

- <kbd>Left</kbd> / <kbd>Right</kbd>: control volume
- <kbd>Up</kbd> / <kbd>Down</kbd>: next or previous track / option
- <kbd>Enter</kbd>: activate the current option
- <kbd>Tab</kbd>: open/close the menu
- <kbd>Esc</kbd>: go back

You can also set hotkeys to control various functions of the app. This can also be helpful for instance if you want to bind a knob or a button on your HOTAS to a function in the app. See the [Hotkey section](#Hotkeys) for more details.

### <a name="Mouse"></a>Mouse controls

- [Left Click]: activate the option
- [Right Click]: open/close the menu
- [MouseWheel]: increase/decrease volume

**Tip**: if you click on the header bar (where the clock is), you go up a menu level. Very helpful when navigating the menus.

<iframe width="560" height="315" src="https://www.youtube.com/embed/tArx1QL-ISY" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>

### <a name="VoiceAttack"></a>VoiceAttack plugin

If you want to use the app together with the awesome [VoiceAttack](https://voiceattack.com/) software, you will need the plugin to create the necessary interface.

In the installation folder you will also find a VoiceAttack folder (this is usually at `%LocalAppData%\Programs\EliteG19s\VoiceAttack` or `C:\Users\You\AppData\Local\Programs\EliteG19s\VoiceAttack`). You will want to copy the contents of the Apps folder there to your VoiceAttack's Apps folder (usually at `C:\Program Files (x86)\VoiceAttack\Apps`). This will allow the app and VoiceAttack to communicate.

Also make sure that you have ticked the box 'Enable Plugin Support' in VoiceAttack's settings screen.

In the app's VoiceAttack folder you will also find an example VAP profile that you can import to see some examples on how you can use the plugin. The [reference sheet is found here](VAProfile.html).

The VoiceAttack plugin supports the following commands, that you provide as the context:

| Command              | Example                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------------- | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `volume`             | `volume:+5`               | Change the overall volume in EliteG19s                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| `mute`               | `mute`                    | Mute/Unmute EliteG19s                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| `traffic volume`     | `traffic volume:-5`       | Change the volume of Space Traffic Control                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `screen`             | `screen:Orrery`           | Switch EliteG19s to the specified screen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| `radio`              | `radio:Lave Radio`        | Play a specific radio station                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| `spotify`            | `spotify:Elite Dangerous` | Play a specific Spotify playlist                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `podcast`            | `podcast:Lave Radio`      | Play the latest episode of the specified podcast                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `stream url`         | `stream url:https://xxx`  | Stream music from a url (can also be a link to soundcloud, or youtube)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| `play folder`        | `play folder:C:\Music`    | Play music from a folder on disk                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `youtube`            | `youtube:Isinona`         | Play a YouTube preset                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| `next track`         | `next track`              | Go to next track                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `previous track`     | `previous track`          | Go to previous track                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| `skip back`          | `skip back`               | Skip back 30 seconds in the current track                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| `skip forward`       | `skip forward`            | Skip forward 30 seconds in the current track                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| `pause music`        | `pause music`             | Pause/resume the current music track                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| `shuffle music`      | `shuffle music`           | Toggle shuffling of music tracks                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `stop music`         | `stop music`              | Stop all currently playing music                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `what's playing`     | `what's playing`          | Check what's currently playing and store this information in the following VoiceAttack text variables: `EliteG19s_Current_Station`, `EliteG19s_Current_Artist`, `EliteG19s_Current_Album`, `EliteG19s_Current_Title`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| `status`             | `status`                  | Retrieve status information and store this information in the following VoiceAttack text variables: `EliteG19s_CommanderName`, `EliteG19s_Credits`, `EliteG19s_CombatRank`, `EliteG19s_CQCRank`, `EliteG19s_ExplorationRank`, `EliteG19s_TradeRank`, `EliteG19s_FederationRank`, `EliteG19s_EmpireRank`, `EliteG19s_GameMode`, `EliteG19s_IsGameInBeta`, `EliteG19s_IsInSuperCruise`, `EliteG19s_Ship`, `EliteG19s_ShipName`, `EliteG19s_ShipId`, `EliteG19s_CurrentSystem`, `EliteG19s_IsDocked`, `EliteG19s_IsLanded`, `EliteG19s_ClosestStation`, `EliteG19s_ClosestBody`, `EliteG19s_BodyLatitude`, `EliteG19s_BodyLongitude`, `EliteG19s_AssignedLandingPad`, `EliteG19s_IsCockpitBreached`, `EliteG19s_IsInCrew`. |
| `traffic`            | `traffic:on`              | Turn Space Traffic Control on or off                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| `traffic volume`     | `traffic volume:+5`       | Change the volume of Space Traffic Control                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `npc volume`         | `npc volume:+5`           | Change the volume of NPCs                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| `orrery zoom in`     | `orrery zoom in`          | Zoom in on the orrery view                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| `orrery zoom out`    | `orrery zoom out`         | Zoom out on the orrery view                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `orrery time faster` | `orrery time faster`      | Speed up time on the orrery view                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `orrery time slower` | `orrery time slower`      | Slow down time on the orrery view                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| `orrery reset view`  | `orrery reset view`       | Reset zoom on the orrery view                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| `visualization`      | `visualization:Starfield` | Switch to one of the visualization modes: Cassette, Orrery, Starfield, Equalizer, Spectrogram, Waveform, Full Screen Equalizer, Full Screen Cover Art                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| `button`             | `button:menu`             | Simulate button press of a button. Choose from `up`, `down`, `left`, `right`, `menu`, `ok`, `cancel`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| `show message`       | `show message:text`       | Display a text on the EliteG19s display                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

Valid screen names are:

- `Menu`
- `About`
- `AudioVisualization`
- `Options`
- `Radio`
- `Spotify`
- `Status`
- `Orrery`
- `News`
- `WhatsNew`
- `Youtube`
- `Twitch`
- `Camera`
- `GPS`

#### The `what's new` variables:

| Variable Name               | Type | Contents                                         |
| --------------------------- | ---- | ------------------------------------------------ |
| `EliteG19s_Current_Station` | Text | The current (radio) station                      |
| `EliteG19s_Current_Artist`  | Text | The artist of the current track (if known)       |
| `EliteG19s_Current_Album`   | Text | The album title for the current track (if known) |
| `EliteG19s_Current_Title`   | Text | Title of the current track                       |

#### The `status` variables:

Please note that BodyLongitude/BodyLatitude have been renamed to CurrentLongitude/CurrentLatitude.

| Variable Name                    | Type | Contents                                      |
| -------------------------------- | ---- | --------------------------------------------- |
| `EliteG19s_AssignedLandingPad`   | Int  | Landing pad assigned during docking procedure |
| `EliteG19s_ClosestBody`          | Text | Name of closest planet (if known)             |
| `EliteG19s_ClosestStation`       | Text | Name of closest station (if known)            |
| `EliteG19s_CombatRank`           | Text | Current combat rank (updated on load)         |
| `EliteG19s_CommanderName`        | Text | Name of current Commander                     |
| `EliteG19s_CQCRank`              | Text | Current CQC rank (updated on load)            |
| `EliteG19s_Credits`              | Dec  | Number of credits (updated on load)           |
| `EliteG19s_CurrentSystem`        | Text | Name of current star system                   |
| `EliteG19s_EmpireRank`           | Text | Current Empire rank (updated on load)         |
| `EliteG19s_ExplorationRank`      | Text | Current exploration rank (updated on load)    |
| `EliteG19s_FederationRank`       | Text | Current Federation rank (updated on load)     |
| `EliteG19s_GameMode`             | Text | Current game mode (Open / Private / Solo)     |
| `EliteG19s_IsCockpitBreached`    | Bool | Has the cockpit been breached                 |
| `EliteG19s_IsGameInBeta`         | Bool | Is the game currently in beta                 |
| `EliteG19s_IsInCrew`             | Bool | Are you in a multicrew session                |
| `EliteG19s_IsInWitchspace`       | Bool | Are you in witchspace                         |
| `EliteG19s_Ship`                 | Text | Current type of ship                          |
| `EliteG19s_ShipName`             | Text | Current name of ship                          |
| `EliteG19s_ShipId`               | Text | Current identifier of ship                    |
| `EliteG19s_TradeRank`            | Text | Current trade rank (updated on load)          |
| `EliteG19s_IsDocked`             | Bool | Are you currently docked                      |
| `EliteG19s_IsLanded`             | Bool | Are you currently landed                      |
| `EliteG19s_IsInSuperCruise`      | Bool | Are you flying in supercruise                 |
| `EliteG19s_CurrentLongitude`     | Dec  | Current Longitude (or 999 if unknown)         |
| `EliteG19s_CurrentLatitude`      | Dec  | Current Latitude (or 999 if unknown)          |
| `EliteG19s_CurrentAltitude`      | Dec  | Current Altitude (or -1 if unknown)           |
| `EliteG19s_CurrentHeading`       | Dec  | Current Heading (if available)                |
| `EliteG19s_Firegroup`            | Int  | Active firegroup                              |
| `EliteG19s_GuiFocus`             | Text | Ship's GUI element that has the focus         |
| `EliteG19s_PipsSystem`           | Int  | Pips to system (0-8, in halves)               |
| `EliteG19s_PipsEngine`           | Int  | Pips to engine (0-8, in halves)               |
| `EliteG19s_PipsWeapons`          | Int  | Pips to weapons (0-8, in halves)              |
| `EliteG19s_IsDocked`             | Bool | Docked, (on a landing pad)                    |
| `EliteG19s_IsLanded`             | Bool | Landed, (on planet surface)                   |
| `EliteG19s_IsLandingGearDown`    | Bool | Landing Gear Down                             |
| `EliteG19s_IsShieldsUp`          | Bool | Shields Up                                    |
| `EliteG19s_IsInSuperCruise`      | Bool | Supercruise                                   |
| `EliteG19s_IsFlightAssistOff`    | Bool | FlightAssist Off                              |
| `EliteG19s_IsHardpointsDeployed` | Bool | Hardpoints Deployed                           |
| `EliteG19s_IsInWing`             | Bool | In Wing                                       |
| `EliteG19s_IsLightsOn`           | Bool | LightsOn                                      |
| `EliteG19s_IsCargoScoopDeployed` | Bool | Cargo Scoop Deployed                          |
| `EliteG19s_IsSilentRunning`      | Bool | Silent Running                                |
| `EliteG19s_IsScoopingFuel`       | Bool | Scooping Fuel                                 |
| `EliteG19s_IsSrvHandbrake`       | Bool | Srv Handbrake                                 |
| `EliteG19s_IsSrvTurret`          | Bool | Srv Turret                                    |
| `EliteG19s_IsSrvUnderShip`       | Bool | Srv UnderShip                                 |
| `EliteG19s_IsSrvDriveAssist`     | Bool | Srv DriveAssist                               |
| `EliteG19s_IsFsdMassLocked`      | Bool | Fsd MassLocked                                |
| `EliteG19s_IsFsdCharging`        | Bool | Fsd Charging                                  |
| `EliteG19s_IsFsdCooldown`        | Bool | Fsd Cooldown                                  |
| `EliteG19s_IsLowFuel`            | Bool | Low Fuel ( < 25% )                            |
| `EliteG19s_IsOverHeating`        | Bool | Over Heating ( > 100% )                       |
| `EliteG19s_HasLatLong`           | Bool | Has Lat Long                                  |
| `EliteG19s_IsInDanger`           | Bool | Is In Danger ( <u>/!\\</u> icon )             |
| `EliteG19s_IsBeingInterdicted`   | Bool | Being Interdicted                             |
| `EliteG19s_IsInMainShip`         | Bool | In MainShip                                   |
| `EliteG19s_IsInFighter`          | Bool | In Fighter                                    |
| `EliteG19s_IsInSrv`              | Bool | In SRV                                        |

### <a name="Hotkeys"></a>Hotkey support

The app also supports hotkeys. This makes it a lot easier to map buttons to
control the app directly. For instance, on my X-55 I have set a dial button to
control the volume, and a switch to select the status screen.
You set the hotkeys in the options.json file (see below). Each hotkey setting
is either a button press or a function.

Button presses look like this:

    {
      "Function": "Up",
      "UseAlt": true,
      "UseCtrl": true,
      "UseShift": true,
      "UseWin": false,
      "Key": "F5",
      "IsEnabled": false
    },

This maps the <kbd>Alt</kbd>+<kbd>F5</kbd> to the Up button in the app.
The `UseAlt/Ctrl/Shift/Win` modifiers describe if the key needs to pressed with
one of these keys in unison.

The `Key` parameter is the technical name for the key. You can find the
[full list here](<https://msdn.microsoft.com/en-us/library/system.windows.forms.keys(v=vs.110).aspx>). This list also includes codes for multimedia keyboards (keys for volume control, next track, etc.)

Most of the time it is exactly what you would suspect, but
sometimes there can be small differences (`D7` for the <kbd>7</kbd> key in the top row
of your keyboard for instance, but it's `NumPad7` for the <kbd>7</kbd> key on the Num Pad).
Check the list above to make sure!

Finally, the `IsEnabled` property just enables or disables the hotkey. Make sure
to set `IsEnabled` to `true` if you want to use the hotkey!

Apart from button presses, you can also activate certain functions in the app
with a hotkey.

A function looks like this:

    {
      "Function": "Screen Status",
      "UseAlt": true,
      "UseCtrl": true,
      "UseShift": true,
      "UseWin": false,
      "Key": "F6",
      "IsEnabled": true
    },

This maps <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>F6</kbd> to
switch the app to the Status screen. For valid screen names, check out the section
above.

Other functions that are currently available are:

- `Volume Up`
- `Volume Down`
- `Mute`
- `Traffic Volume Up`
- `Traffic Volume Down`
- `NPC Volume Up`
- `NPC Volume Down`
- `Next Screen`
- `Previous Screen`
- `Show` - this will bring the first EliteG19s window to the front
- `Visualization <Name>` - show a specific audio visualization, choose from Cassette, Orrery, Starfield, Equalizer, Spectrogram, Waveform, Full Screen Equalizer, Full Screen Cover Art
- `Screen <Name>` - switch to the desired screen
- `Next Track`
- `Previous Track`
- `Pause`
- `Shuffle`
- `Orrery Zoom In`
- `Orrery Zoom Out`
- `Orrery Time Faster`
- `Orrery Time Slower`
- `Orrery Reset View`

### <a name="Orrery"></a>Orrery view

On the Orrery screen you can use the cursor keys to control the pitch and zoom of the view. These changes are subsequently also used when you switch to the orrery audio visualization.

On the screen you will notice that bodies are highlighted to show specific information on them: is a planet landable, can a star be scooped, how far away is it from the main star?

If you are close to a body, or if you've just scanned one, it will be highlighted by a blue marker.

You can click on a star or planet to highlight it.

The hamburger icon (activate it by pressing <kbd>Enter</kbd>, <kbd>OK</kbd>, or clicking on it) opens a menu where you can zoom in and out, speed up or slow down time
and even open up a custom orrery view, other than the system you're currently flying in.

There is also _experimental_ keyboard support. This will need some finetuning, but feel free to play around with it and give me your feedback.

| Key              | Effect            |
| ---------------- | ----------------- |
| <kbd>W</kbd>     | Move Up           |
| <kbd>A</kbd>     | Move Left         |
| <kbd>S</kbd>     | Move Right        |
| <kbd>D</kbd>     | Move Down         |
| <kbd>Up</kbd>    | Move Forward      |
| <kbd>Down</kbd>  | Move Backward     |
| <kbd>Left</kbd>  | Rotate view left  |
| <kbd>Right</kbd> | Rotate view right |
| <kbd>+</kbd>     | Zoom in           |
| <kbd>-</kbd>     | Zoom out          |
| <kbd>&lt;</kbd>  | Slow down time    |
| <kbd>&gt;</kbd>  | Speed up time     |
| <kbd>Home</kbd>  | Reset view        |

### <a name="GPS"></a>GPS view

The GPS screen allows you to see where you need to go when you're in your SRV or in low orbital flight.
You can set waypoints, or complete itineraries, which can be saved in a file `waypoints.json` (in the same location as the options file mentioned below).

It can be very helpful when you found that place where a bunch of canisters have been dumped and you need a couple trips to your ship to retrieve them all.
Or when you want to take that particular scenic route that you like.
Or when there is a mysterious location you want bookmarked and not bothered by looking up the coordinates all the time.

A helpful arrow will point you in the right direction.

Note however that you will need to manually enable the GPS functionality. When enabled, the app will push F10 every two seconds. This creates a screenshot AND logs the coordinates in the player's journal. The app will automatically delete this temporary screenshot and use the location info to determine the correct heading you will need to find your destination.

There is also a race option. When you have selected an itinerary, the waypoints act as checkpoints for either a timed run, or an outrun-like checkpoint-race. You can even select some wacky music to accompany your race!

### <a name="Hue"></a>Philips Hue support

The app now also supports Philips Hue. For this to work you will first need to create an entertainment zone. You can do this in the Hue app, for instance on your mobile phone or tablet.

After that, you can enable Philips Hue support in the app, by checking the Enabled option in the options screen for Hue.

The app will then search for a Hue bridge. If it can find one it will try to connect. Sometimes you will need to set the Hue bridge IP address manually in the options file ([see here](#Options_PhilipsHueSettings_BridgeIP)), because the app can't find the bridge.

When the app has found a bridge, the first time it will ask you to push the Link button within the next 60 seconds. If you do, the app and the bridge will exchange an AppKey and EntertainmentKey. These are stored in the options file and the connection has been successfully established.

The app uses Hue to set overall colors (either by sampling the colors on screen, or by using an in-theme color), and can be used when playing light effects. For example, a pulsing red light is shown when the game finds that you are in danger (near a star, under attack).

## <a name="Lua"></a>Lua scripting support

The EliteG19s app allows you to create Lua scripts to add functionality. For a full description of this option, see the [Scripting page](EliteG19s-Scripting.html).

## <a name="Options"></a>Options.json file

The EliteG19s app uses the `%AppData%\EliteG19s\options.json` (usually `C:\Users\You\AppData\Roaming\EliteG19s\options.json`) file to store
its options. This is a json file which has a specific notation. Feel free to use
a [JSON validator](http://jsonlint.com/) to check you haven't made any typos
before saving any changes to the options file.

Before you start editing these files manually, most options can be set in the options screen of the app itself. That's usually the easiest solution!

This is a list of all options:

| Option                                                                        | Description                                                                                                                                                                                                                                                                                                                            |
| ----------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a name="Options_Version"></a>`Version`                                       | The current version of the app                                                                                                                                                                                                                                                                                                         |
| <a name="Options_Logging"></a>`Logging`                                       | Options for logging to a log.txt file: `"Logging": { "IsEnabled": true, "IsVerbose": false }` Set both values to true for maximum logging when you encounter errors                                                                                                                                                                    |
| <a name="Options_EliteFolder"></a>`EliteFolder`                               | Where to find the E:D installation (is found automatically in most cases)                                                                                                                                                                                                                                                              |
| <a name="Options_MusicFolder"></a>`MusicFolder`                               | Where do you store your music files?                                                                                                                                                                                                                                                                                                   |
| <a name="Options_JournalsFolder"></a>`JournalsFolder`                         | Optional setting to explicitly set the folder where the Journal files can be found                                                                                                                                                                                                                                                     |
| <a name="Options_InitialVolume"></a>`InitialVolume`                           | The initial volume level of the app (between 0.0 and 1.0)                                                                                                                                                                                                                                                                              |
| <a name="Options_DisplayOptions"></a>`DisplayOptions`                         | Display settings are stored here ([see below](#DisplayOptions))                                                                                                                                                                                                                                                                        |
| <a name="Options_AudioVisualizationOptions"></a>`AudioVisualizationOptions`   | Options for audio visualizations                                                                                                                                                                                                                                                                                                       |
| <a name="Options_IsShowGPSInSRV"></a>`IsShowGPSInSRV`                         | Automatically switch to GPS when in SRV                                                                                                                                                                                                                                                                                                |
| <a name="Options_FavoriteStarSystems"></a>`FavoriteStarSystems`               | A list of favorite star systems for the orrery screen's Favorites menu                                                                                                                                                                                                                                                                 |
| <a name="Options_RadioStations"></a>`RadioStations`                           | A list of radio stations to use ([see below](#RadioStations))                                                                                                                                                                                                                                                                          |
| <a name="Options_TVStations"></a>`TVStations`                                 | A list of YouTube playlists to use ([see below](#TVStations))                                                                                                                                                                                                                                                                          |
| <a name="Options_SpotifyPlaylists"></a>`SpotifyPlaylists`                     | A list of Spotify playlists to use ([see below](#SpotifyPlaylists))                                                                                                                                                                                                                                                                    |
| <a name="Options_Podcasts"></a>`Podcasts`                                     | A list of podcasts that you can listen to                                                                                                                                                                                                                                                                                              |
| <a name="Options_RacingMusic"></a>`RacingMusic`                               | A list of urls to Soundcloud or MP3 files to use when racing with the GPS view                                                                                                                                                                                                                                                         |
| <a name="Options_TwitchChannels"></a>`TwitchChannels`                         | A list of Twitch channels to show always                                                                                                                                                                                                                                                                                               |
| <a name="Options_OnTopReplica"></a>`OnTopReplica`                             | Options to automatically start the OnTopReplica app ([see below](#OnTopReplicaSettings))                                                                                                                                                                                                                                               |
| <a name="Options_SpaceTrafficControlOptions"></a>`SpaceTrafficControlOptions` | Options for space traffic control ([see below](#SpaceTrafficControlOptions))                                                                                                                                                                                                                                                           |
| <a name="Options_IsConvertScreenshots"></a>`IsConvertScreenshots`             | (true/false) allows the app to automatically convert the game's screenshots to a much smaller JPG format and include metadata on where the shot was taken.                                                                                                                                                                             |
| <a name="Options_CustomColorMatrix"></a>`CustomColorMatrix`                   | You can set a custom color matrix here to change the app's colors. This overrides any setting you might have in Elite. [Look here to sample the options](http://arkku.com/elite/hud_editor/). This entry should look like this: <br> <code>"CustomColorMatrix": { "Red": "0.31, 0, 1", "Green": "0, 1, 0", "Blue": "1, 0, 0" },</code> |
| <a name="Options_LogitechSettings"></a>`LogitechSettings`                     | Settings to control Logitech keyboards ([see below](#LogitechSettings))                                                                                                                                                                                                                                                                |
| <a name="Options_IsUseGameTime"></a>`IsUseGameTime`                           | (true/false) display game time or local time in the app's display                                                                                                                                                                                                                                                                      |
| <a name="Options_IsUseDiscordRichPresence"></a>`IsUseDiscordRichPresence`     | (true/false) show your current position in Discord                                                                                                                                                                                                                                                                                     |
| <a name="Options_DefaultTTSVoice"></a>`DefaultTTSVoice`                       | If you have a preferred default text-to-speech voice, set it here, otherwise leave it at Default                                                                                                                                                                                                                                       |
| <a name="Options_ArxWidthHeightRatio"></a>`ArxWidthHeightRatio`               | (number) set the ratio of the Arx screen width as a percentage of the height (100 is square, 105 is a bit wider, 95 is a bit smaller). Remove the option to use the full width of the screen.                                                                                                                                          |
| <a name="Options_ArxAnimationLevel"></a>`ArxAnimationLevel`                   | (none/semi/full) can the Arx app use animation, choose one of the options                                                                                                                                                                                                                                                              |
| <a name="Options_HotKeys"></a>`HotKeys`                                       | Map hotkeys to app functions ([see above](#Hotkeys))                                                                                                                                                                                                                                                                                   |
| <a name="Options_NewsTicker"></a>`NewsTicker`                                 | Set different RSS tickers to use in the news ticker                                                                                                                                                                                                                                                                                    |
| <a name="Options_GracenoteId"></a>`GracenoteId`                               | Do not change - used to retrieve album art                                                                                                                                                                                                                                                                                             |
| <a name="Options_PhilipsHue"></a>`PhilipsHue`                                 | Settings for Philips Hue lights ([see below](#PhilipsHueSettings))                                                                                                                                                                                                                                                                     |
| <a name="Options_AmbilightUpdateInterval"></a>`AmbilightUpdateInterval`       | The delay between reads of the screen by the Ambilight routine                                                                                                                                                                                                                                                                         |
| <a name="Options_IPCamera"></a>`IPCamera`                                     | Setting to display view of MJPEG IP Camera ([see below](#IPCameraSettings))                                                                                                                                                                                                                                                            |

### <a name="DisplayOptions"></a>Setting the display options

The `DisplayOptions` section of the options.json file controls how and when window are opened automatically. Saved window positions are stored here as well when the app exits.

This section contains the following settings:

| Setting                                                                    | Description                                                                                                                                       |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a name="Options_DisplayOptions_UseWindow"></a>`UseWindow`                 | Start with a regular window showing (never/always/auto)                                                                                           |
| <a name="Options_DisplayOptions_InitialScreen"></a>`InitialScreen`         | The name of the screen to start the app with                                                                                                      |
| <a name="Options_DisplayOptions_IsUseDirect3D"></a>`IsUseDirect3D`         | (true/false) Use Direct3D for the non-Logitech windows (`true` improves performance but sometimes causes compatibility issues                     |
| <a name="Options_DisplayOptions_SaveWindowsOnExit"></a>`SaveWindowsOnExit` | (true/false) remember open windows when exiting and restore them when the app restarts                                                            |
| <a name="Options_DisplayOptions_DisplayMessages"></a>`DisplayMessages`     | (all, primary, secondary) where to display messages (such as when friends come online, or when displaying an interactice traffic control message) |
| <a name="Options_DisplayOptions_Windows"></a>`Windows`                     | This is where saved windows are stored. Use the `SaveWindowsOnExit` option to have the app create these automatically                             |

### <a name="RadioStations"></a>Updating the radio stations

There is not yet an option in the app itself to edit the list of online radio stations.
For this you will need to open the options.json file and look for the section marked
"`RadioStations`". You will find several sections there, marked by curly braces. An example is:

    {
      "Name": "Radio Sidewinder",
      "Url": "http://www.radiosidewinder.com/radiosidewinder.m3u"
    },

Sometimes you will also see a setting called "`OriginalUrl`" in there.
This is added automatically if the radiostation forwards to a different url.
The original is saved just in case the forwarding is ever updated.

You can edit the radio stations here. Make sure that you use a direct link to the MP3 stream.
Often this is the link you get for the ".pls" or ".m3u" file from the station's site.
If you cannot find that, look for a link that offers to listen to the station in an
external media player such as VLC or iTunes.

Also, please make sure that the stream is offered as an MP3 stream. This is the only type
of audio stream that the app currently understands. AAC or other types of streams will not play.

### <a name="TVStations"></a>Updating the tv stations (Youtube channels)

There is not yet an option in the app itself to edit the list of Youtube channels or videos. For this you will need to open the options.json file and look for the section marked "`TVStations`". You will find several sections there, marked by curly braces. An example is:

    {
      "Name": "Isinona",
      "PlaylistId": "UUjgBlzLxsgbVuHfZPe0AeIg",
      "Randomized": false
    },

The PlaylistId is basically the bit in the url after `https://www.youtube.com/channel/`. If Randomized is set to `true`, it will shuffle the videos in the playlist.

You can also link directly to specific videos:

    {
      "Name": "Elite Dangerous Space Legs leaked video",
      "VideoId": "4M8ZeHZSZ3o"
    },

### <a name="SpotifyPlaylists"></a>Updating the Spotify playlists

You can define a set of playlists in the options file itself if you like to have a very specific list of Elite playlists. However, there is not yet an option in the app itself to edit the list of Spotify playlists that you can choose from. For this you will need to open the options.json file and look for the section marked `"SpotifyPlaylists`". You will find several sections there, marked by curly braces. An example is:

    {
      "Name": "Hot New Dance Tracks",
      "SpotifyLink": "spotify:user:spotify:playlist:37i9dQZF1DWWrJKwf0q9nn"
    },

In the Spotify app you can click the Share button to copy the Spotify URI, which is what you put in the "SpotifyLink" in this option. You can also put in a Spotify URL that looks like this: [https://open.spotify.com/user/spotify/playlist/37i9dQZF1DWWrJKwf0q9nn](https://open.spotify.com/user/spotify/playlist/37i9dQZF1DWWrJKwf0q9nn).

### <a name="OnTopReplicaSettings"></a>Options to automatically start OnTopReplica

The `OnTopReplica` section of the options contains settings to be able to automatically start OnTopReplica when the first window is opened:

| Setting                                                                  | Description                                                                                                                                                                                                                                                                                                                         |
| ------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a name="Options_OnTopReplica_AttachFirstWindow"></a>`AttachFirstWindow` | (true/false) attach OnTopReplica to the first window                                                                                                                                                                                                                                                                                |
| <a name="Options_OnTopReplica_ExePath"></a>`ExePath`                     | Path to OnTopReplica.exe, eg. `"C:\\Path\\OnTopReplica.exe"` (note that the JSON format requires backslashes to be doubled)                                                                                                                                                                                                         |
| <a name="Options_OnTOpReplica_Parameters"></a>`Parameters`               | How to call OnTopreplica, eg. `"--windowId=$HWND$ --size=$WIDTH$,$HEIGHT$}`<br> Sensible defaults are provided (using the default install location and showing the window semi-transparent top right), but you are free to change them. Use the placeholders `$HWND$`, `$WINDOW_TITLE$`, `$WIDTH$`, and `$HEIGHT$` where necessary. |

### <a name="SpaceTrafficControlOptions"></a>Options for Space Traffic Control and NPC voices

The `SpaceTrafficControlOptions` section of the options file contains settings to control Space Traffic Control and NPC voices.

| Setting                                                                                        | Description                                                                                                                                                                                |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <a name="Options_SpaceTrafficControlOptions_EnableOnStart"></a>`EnableOnStart`                 | (true/false) to enable Space Traffic Control upon startup                                                                                                                                  |
| <a name="Options_SpaceTrafficControlOptions_Volume"></a>`Volume`                               | (0.0-1.0) the volume of Space Traffic Control                                                                                                                                              |
| <a name="Options_SpaceTrafficControlOptions_Density"></a>`Density`                             | increase or decrease the amount of Space Traffic Control                                                                                                                                   |
| <a name="Options_SpaceTrafficControlOptions_UseSoundEffects"></a>`UseSoundEffects`             | (true/false) enable sound effects on Space Traffic Control voices                                                                                                                          |
| <a name="Options_SpaceTrafficControlOptions_OnlyInSuperCruise"></a>`OnlyInSuperCruise`         | (true/false) only have Space Traffic Control active while in Supercruise                                                                                                                   |
| <a name="Options_SpaceTrafficControlOptions_ShowTrafficSubtitles"></a>`ShowTrafficSubtitles`   | (true/false) show Space Traffic Control subtitles                                                                                                                                          |
| <a name="Options_SpaceTrafficControlOptions_StartDelay"></a>`StartDelay`                       | a delay (in milliseconds) before Space Traffic Control starts transmitting - use this if you want another app to finish its script first for instance                                      |
| <a name="Options_SpaceTrafficControlOptions_TrafficControlLocalized">`TrafficControlLocalized` | (true/false) localize space traffic control in the game's language where avaiable (currently English and Spanish)                                                                          |
| <a name="Options_SpaceTrafficControlOptions_NPCVoicesEnabled"></a>`NPCVoicesEnabled`           | (true/false) enable NPC voices                                                                                                                                                             |
| <a name="Options_SpaceTrafficControlOptions_NPCVolume"></a>`NPCVolume`                         | (0.0-1.0) the volume of NPC and CMDR voices                                                                                                                                                |
| <a name="Options_SpaceTrafficControlOptions_CMDRVoicesEnabled"></a>`CMDRVoicesEnabled`         | (true/false) enable CMDR voices                                                                                                                                                            |
| <a name="Options_SpaceTrafficControlOptions_CMDRVoicesLocalized"></a>`CMDRVoicesLocalized`     | (true/false) localize CMDR voices (eg if you play in German, all CMDR speech will use a German text to speech voice)                                                                       |
| <a name="Options_SpaceTrafficControlOptions_CMDRVoiceLanguage"></a>`CMDRVoiceLanguage`         | (`Game` \| `EN` \| `DE` \| `FR` \| `ES` \| `RU`) specifically set the language to use for CMDR text-to-speech. Use this for instance to force it to English if you run a non-English game. |
| <a name="Options_SpaceTrafficControlOptions_VoiceOptions"></a>`VoiceOptions`                   | specific options to be set per installed voice (see below)                                                                                                                                 |

### <a name="LogitechSettings"></a>Options for Logitech keyboards

The `LogitechSettings` section of the options file contains settings for Logitech keyboards.

| Setting                                                                        | Description                                                                                         |
| ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| <a name="Options_LogitechSettings_SetBackgroundColor"></a>`SetBackgroundColor` | Allow the app to set an overall "background" in-theme color for the LED lights                      |
| <a name="Options_LogitechSettings_PlayEffects"></a>`PlayEffects`               | Allow the app to play LED light effects when certain events occur (such as jumping into witchspace) |
| <a name="Options_LogitechSettings_Ambilight"></a>`Ambilight`                   | The LEDs will use the average color of the screen to set the background color                       |

### <a name="PhilipsHueSettings"></a>Options for Philips Hue

The `PhilipsHue` section of the options file contains settings for Philips Hue lights.

| Setting                                                                      | Description                                                                                                                                                                               |
| ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <a name="Options_PhilipsHueSettings_IsEnabled"></a>`IsEnabled`               | (true/false) enable Philips Hue interface                                                                                                                                                 |
| <a name="Options_PhilipsHueSettings_BridgeIP"></a>`BridgeIP`                 | the IP address of the Philips Hue bridge to communicate with. The app will try to find it by querying the local network. Because this sometimes fails, you can also set it here manually. |
| <a name="Options_PhilipsHueSettings_AppKey"></a>`AppKey`                     | This is set automatically by the app when a connection with the Bridge has been set up                                                                                                    |
| <a name="Options_PhilipsHueSettings_EntertainmentKey"></a>`EntertainmentKey` | This is set automatically by the app when a connection with the Bridge has been set up                                                                                                    |
| <a name="Options_PhilipsHueSettings_Intensity"></a>`Intensity`               | (0.0 - 1.0) How bright should the light bulbs get                                                                                                                                         |
| <a name="Options_PhilipsHueSettings_Ambilight"></a>`Ambilight`               | Sample the game screen to determine a color setting for the Hue lights                                                                                                                    |
| <a name="Options_PhilipsHueSettings_PlayEffects"></a>`PlayEffects`           | Allow the app to play Hue light effects when certain events occur (such as jumping into witchspace)                                                                                       |

### <a name="IPCameraSettings"></a>Options for IP Cameras

The `IPCamera` section of the options file contains settings for Philips Hue lights.

| Setting                                                                          | Description                                                                                                                        |
| -------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| <a name="Options_IPCamera_MJPEGCameraUrl"></a>`MJPEGCameraUrl`                   | Set this to the video feed of an MJPEG IP camera and have the app act as a motion detector. Useful if you have tiny CMDRs at home. |
| <a name="Options_IPCamera_CameraMotionSensitivity"></a>`CameraMotionSensitivity` | (0-1) A number between 0 and 1 that says how sensitive the motion detection is. The closer to 0 the quicker it alerts you.         |
| <a name="Options_IPCamera_AutoStart"></a>`AutoStart`                             | Automatically connect with the camera when the app starts.                                                                         |

## <a name="MoreVoices"></a>Windows 10 Additional Voices

_This section is copied from a relevant Reddit post
[here](https://www.reddit.com/r/EliteDangerous/comments/5d02vv/if_you_use_voiceattack_eddi_or_any_other/)._

When Microsoft released Windows 10, they included the Text-to-Speech voices that were created for Windows Mobile.  
Additionally, when you install some of the language packs from the Region and Language options in windows, you are also given the option to download a related voice pack for that language that includes both a male and a female mobile voice.

As an example, windows 10 comes with the following two mobile voicepacks if your region is English/United States:

- Microsoft Mark Mobile - English (United States)
- Microsoft Zira Mobile - English (United States)

For English you can also additionally install the following language packs and download the speech library for it, each one includes at least 1 new male and 1 new female voice pack:

- English - Australia;
- English - UK;
- English - Canada;
- English - India;

In order to make these additional voices available for the companion app, you will need to copy some information. You can do this manually (see the Reddit post for this), or use this handy PowerShell script.

1. Click Start
2. Type `Powershell`
3. Right click the search result and choose `Run as Administrator`.
4. Copy and paste the script into the console. Press Enter.

[]()

    $sourcePath = 'HKLM:\software\Microsoft\Speech_OneCore\Voices\Tokens' #Where the OneCore voices live
    $destinationPath = 'HKLM:\SOFTWARE\Microsoft\Speech\Voices\Tokens' #For 64-bit apps
    $destinationPath2 = 'HKLM:\SOFTWARE\WOW6432Node\Microsoft\SPEECH\Voices\Tokens' #For 32-bit apps
    $listVoices = Get-ChildItem $sourcePath
    foreach($voice in $listVoices)
    {
    $source = $voice.PSPath #Get the path of this voices key
    copy -Path $source -Destination $destinationPath -Recurse
    copy -Path $source -Destination $destinationPath2 -Recurse
    }

## <a name="Troubleshooting"></a>Troubleshooting

If you run into any trouble with my little companion app for Elite,
please check the following:

- Make sure that you have the latest Logitech Gaming Software installed for
  Logitech keyboard support.
  [Download it here](http://support.logitech.com/en_us/software/lgs).
- Make sure you have the 32 bit version of the C++ 2012 redistributables
  installed from [Microsoft](http://www.microsoft.com/en-us/download/details.aspx?id=30679).
- Check your anti-virus software for false positives.
- Please reinstall the latest version of the app and its dependencies
  from: https://apps.magicmau.nl/EliteG19s/EliteG19s-latest.msi.

### <a name="AppWillNotStartAfterUpgrade"></a>App will not start after an upgrade

If the app does not start after upgrading to the new version, it could be that files from the previous version have
not been completely removed by the installation procedure. This happens most often if the new version is installed
in a different location than before.

In this case, please manually remove all other files from previous versions of the app.

1. First uninstall the current version of the app using "Add/Remove Programs" or "Settings>Apps".
2. Manually delete any files that have not been removed automatically. The default location for the application is `C:\Users\[YourName]\AppData\Local\Programs\EliteG19s`, unless you specified a custom location during the installation process.
3. Reinstall the latest version of the app using [this link](https://apps.magicmau.nl/EliteG19s/EliteG19s-latest.msi).

### Reinstall the latest version

If everything seems to fail, try a full reinstall by manually deleting all existing files first. This sometimes solves some unexplainable issues :)

First, uninstall normally (through Programs & Features). Optionally, also remove any remaining files by following the step below.

<b>_However, as this step involves manually deleting files, be careful and do this at your own risk!_</b>

You can do this by deleting the files in the folder `C:\Users\[YourName]\AppData\Roaming\EliteG19s` as well as deleting the files in `C:\Users\[YourName]\AppData\Local\Programs\EliteG19s`.

### Send log files

If that does not resolve the problem, allow me to help you.
If the app crashes, it tries to produce a log file, which you can find in the
following folder: `C:\Users\[YourName]\AppData\Roaming\EliteG19s`.

From that folder, please email me the log.txt and options.json file.
You can send them to magicmau [at] gmail.com.

If at all possible, please also enable additional logging before you capture the
log.txt file.

You can do this by opening the options.json file in the folder above. At the top
you will see the following. Please make sure both options are set to true:

    "Logging": {
      "IsEnabled": true,
      "IsVerbose": true
    },

Another way to enable it is through the options in the app itself.
Scroll down to enable the options "Error Logging"
and "Verbose Logging".

After you've restarted the application, additional debugging
information is recorded in the log.txt file.
Please send me that file :)
You can then turn the logging options off if you want.

## <a name="Contact"></a>Contact me

The easiest way to get in touch is through the [Elite forum post](https://forums.frontier.co.uk/showthread.php/226782) for this app,
or find me on the [EliteG19s Discord channel](https://discord.gg/Ew7Baq5).

If you want to contact me, either send me an email (magicmau at gmail dot com), find me on Twitter ([@MagicMau](https://twitter.com/MagicMau))
drop me a PM on Reddit ([/u/MagicMau](https://www.reddit.com/message/compose/?to=MagicMau)), or message me in-game (MagicMau).
