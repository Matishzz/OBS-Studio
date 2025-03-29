<div align="center">
  <img src="https://jdleongomez.info/es/post/obs/featured.png" height="150">
<h3>Installation Manual</h3>
  </a>
  <p>
    Join/follow us on <a href="https://dsc.gg/matishzz-tweak" target="_blank">Discord</a> | <a href="https://x.com/Matishzz" target="_blank">𝕏 (Twitter)</a>
  </p>
  <p>
    <a href="https://github.com/Matishzz/OBS-Studio">Automatic installation</a> ⠂<a href="https://github.com/Matishzz/OBS-Studio/blob/main/Troubleshooting.md">Troubleshooting</a> ⠂ <a href="https://github.com/Matishzz/OBS-Studio/blob/main/AMF%20Options.md">AMF Options</a>
    
  </p>
</div>  

---

<p align="center">
Most of the errors have been clarified in <a href="https://github.com/Matishzz/OBS-Studio/blob/main/Troubleshooting.md">Troubleshooting</a> but it may be present some anomaly that I have not taken into account when making the respective <code>.md</code>, that is why I give the possibility and ease to the user to do it this way, also this gives the possibility to users who do not have the dependencies of Invoke-WebRequest (crucial element in the automatic installation).
</p>

<br>

## 🔗 Installation of OBS Studio
This step is very simple, the only thing we have to do is download the installer of the latest version of <a href="https://obsproject.com/es/download">OBS Studio</a> and run it, you can also install other versions in <a href="https://github.com/obsproject/obs-studio/releases">obs-studio/releases</a> although some old versions have problems with the linking of twitch accounts and may conflict with some configurations due to changes in variables.
> [!WARNING]
> The latest version of OBS Studio containing the <a href="https://obsproject.com/kb/capture-hook-certificate-update">new certificate</a> will be installed, if you experience problems with game capture, please refer to the <a href="https://github.com/Matishzz/OBS-Studio/blob/main/Troubleshooting.md#game-capture-does-not-work-">troubleshooting\capture-hook</a>


## 📌 Running OBS Studio for the first time
When OBS Studio is run for the first time, a folder is created in `%appdata%` which stores the OBS Studio configuration, the strategy I take to import the profiles is to create the `.ini` and `.json` that save the configuration, we can manually open OBS and close it or run this command in CMD
```bash
cd %programfiles%\obs-studio\bin\64bit & powershell Start-Process -FilePath "obs64.exe" -WindowStyle Minimized & timeout /t 3 >nul & powershell stop-process -ProcessName obs64 -Force
```

## 🎈 Configure Global.ini & User.ini
As its name says, this section maintains the global and user configuration of OBS Studio, this configuration is stored in `%appdata%\OBS Studio` and maintains settings such as the current theme, the proportions of the docks among other things, to run the bath that makes this procedure is necessary to first download it and run it.
```batch
( echo [General] & (echo Pre31Migrated=false) & echo MaxLogs=10 & (echo InfoIncrement=-1) & echo ProcessPriority=Normal & (echo EnableAutoUpdates=false) & echo BrowserHWAccel=true & (echo InstallGUID=3ea4eae22cac81a58ea345f51a96d71b602ec233) & echo LastVersion=520093696 & echo. & echo [Video] & (echo Renderer=Direct3D 11) & echo. & echo [Audio] & (echo DisableAudioDucking=true) ) > "%appdata%\obs-studio\Global.ini" & ( echo [General] & (echo Pre19Defaults=false) & echo Pre21Defaults=false & (echo Pre23Defaults=false) & echo Pre24.1Defaults=false & (echo FirstRun=true) & echo SkipUpdateVersion=452984833 & (echo ProcessPriority=Normal) & echo. & echo [Appearance] & (echo Theme=com.obsproject.Yami.Original) & echo. & echo [Basic] & (echo Profile=Matishzz) & echo ProfileDir=Matishzz & (echo SceneCollection=Matishzz) & echo SceneCollectionFile=Matishzz & echo. & echo [BasicWindow] & (echo gridMode=false) & (echo geometry=AdnQywADAAAAAAGkAAAAqgAABqIAAAO+AAABpAAAAMkAAAaiAAADvgAAAAAAAAAAB4AAAAGkAAAAyQAABqIAAAO+) & (echo DockState=AAAA/wAAAAD9AAAAAgAAAAAAAADIAAABg/wCAAAAAfsAAAAUAHMAYwBlAG4AZQBzAEQAbwBjAGsBAAAAFwAAAYMAAAChAP///wAAAAMAAAT/AAABNvwBAAAABfsAAAAWAHMAbwB1AHIAYwBlAHMARABvAGMAawEAAAAAAAAAxQAAAJgA////+wAAAB4AdAByAGEAbgBzAGkAdABpAG8AbgBzAEQAbwBjAGsAAAACogAAATAAAAEwAP////sAAAASAHMAdABhAHQAcwBEAG8AYwBrAQAAAMkAAAJfAAACXwD////7AAAAEgBtAGkAeABlAHIARABvAGMAawEAAAMsAAABHwAAALYA////+wAAABgAYwBvAG4AdAByAG8AbABzAEQAbwBjAGsBAAAETwAAALAAAACwAP///wAABDMAAAGDAAAABAAAAAQAAAAIAAAACPwAAAAA) & (echo ExtraBrowserDocks=[]) & (echo PreviewEnabled=true) & echo AlwaysOnTop=false & (echo SceneDuplicationMode=true) & echo SwapScenesMode=true & (echo ShowContextToolbars=false) & echo EditPropertiesMode=false & (echo VerticalVolControl=true) & echo PreviewProgramMode=true & (echo DocksLocked=false) & echo WarnBeforeStartingStream=false & (echo WarnBeforeStoppingStream=false) & echo WarnBeforeStoppingRecord=false & (echo HideProjectorCursor=false) & echo ProjectorAlwaysOnTop=false & echo. & echo [ScriptLogWindow] & (echo geometry=AdnQywADAAAAAAABAAAAIAAAAlgAAAGvAAAAAQAAACAAAAJYAAABrwAAAAAAAAAAB4AAAAABAAAAIAAAAlgAAAGv) ) > "%appdata%\obs-studio\user.ini"
```

## 🔌 Create Scene
The `global.ini` is configured so that the scene present is for the `matishzz.json` scene, for this run this batch, this configuration brings a filter for the microphone among other things.
```batch
echo { "DesktopAudioDevice1": { "prev_ver": 520093696, "name": "Desktop Audio", "uuid": "c0e58ca7-39fd-4b54-bff0-2b699edc7330", "id": "wasapi_output_capture", "versioned_id": "wasapi_output_capture", "settings": { "device_id": "default" }, "mixers": 255, "sync": 0, "flags": 0, "volume": 1.0, "balance": 0.5, "enabled": true, "muted": false, "push-to-mute": false, "push-to-mute-delay": 0, "push-to-talk": false, "push-to-talk-delay": 0, "hotkeys": { "libobs.mute": [], "libobs.unmute": [], "libobs.push-to-mute": [], "libobs.push-to-talk": [] }, "deinterlace_mode": 0, "deinterlace_field_order": 0, "monitoring_type": 0, "private_settings": {} }, "AuxAudioDevice1": { "prev_ver": 520093696, "name": "Mic/Aux", "uuid": "7c5e6b8f-de66-4cc9-8d60-fd4d2e7f97c3", "id": "wasapi_input_capture", "versioned_id": "wasapi_input_capture", "settings": { "device_id": "default" }, "mixers": 255, "sync": 0, "flags": 0, "volume": 1.0, "balance": 0.5, "enabled": true, "muted": false, "push-to-mute": false, "push-to-mute-delay": 0, "push-to-talk": false, "push-to-talk-delay": 0, "hotkeys": { "libobs.mute": [], "libobs.unmute": [], "libobs.push-to-mute": [], "libobs.push-to-talk": [] }, "deinterlace_mode": 0, "deinterlace_field_order": 0, "monitoring_type": 0, "private_settings": {}, "filters": [ { "prev_ver": 520093696, "name": "Noise Gate - Default", "uuid": "e43ef040-3361-42a5-b13f-46eaf90e4429", "id": "noise_gate_filter", "versioned_id": "noise_gate_filter", "settings": {}, "mixers": 255, "sync": 0, "flags": 0, "volume": 1.0, "balance": 0.5, "enabled": true, "muted": false, "push-to-mute": false, "push-to-mute-delay": 0, "push-to-talk": false, "push-to-talk-delay": 0, "hotkeys": {}, "deinterlace_mode": 0, "deinterlace_field_order": 0, "monitoring_type": 0, "private_settings": {} } ] }, "current_scene": "Scene", "current_program_scene": "Scene", "scene_order": [ { "name": "Scene" } ], "name": "Matishzz", "sources": [ { "prev_ver": 520093696, "name": "Scene", "uuid": "dace504e-59be-4faf-b468-efb3bc89c18a", "id": "scene", "versioned_id": "scene", "settings": { "id_counter": 1, "custom_size": false, "items": [] }, "mixers": 0, "sync": 0, "flags": 0, "volume": 1.0, "balance": 0.5, "enabled": true, "muted": false, "push-to-mute": false, "push-to-mute-delay": 0, "push-to-talk": false, "push-to-talk-delay": 0, "hotkeys": { "OBSBasic.SelectScene": [] }, "deinterlace_mode": 0, "deinterlace_field_order": 0, "monitoring_type": 0, "private_settings": {} } ], "groups": [], "quick_transitions": [ { "name": "Cut", "duration": 300, "hotkeys": [], "id": 1, "fade_to_black": false }, { "name": "Fade", "duration": 300, "hotkeys": [], "id": 2, "fade_to_black": false }, { "name": "Fade", "duration": 300, "hotkeys": [], "id": 3, "fade_to_black": true } ], "transitions": [], "saved_projectors": [], "current_transition": "Fade", "transition_duration": 300, "preview_locked": false, "scaling_enabled": false, "scaling_level": 0, "scaling_off_x": 0.0, "scaling_off_y": 0.0, "virtual-camera": { "type2": 3 }, "modules": { "scripts-tool": [], "output-timer": { "streamTimerHours": 0, "streamTimerMinutes": 0, "streamTimerSeconds": 30, "recordTimerHours": 0, "recordTimerMinutes": 0, "recordTimerSeconds": 30, "autoStartStreamTimer": false, "autoStartRecordTimer": false, "pauseRecordTimer": true }, "auto-scene-switcher": { "interval": 300, "non_matching_scene": "", "switch_if_not_matching": false, "active": false, "switches": [] }, "captions": { "source": "", "enabled": false, "lang_id": 1033, "provider": "mssapi" } }, "resolution": { "x": 1280, "y": 720 }, "version": 2 }>> "%appdata%\obs-studio\basic\scenes\Matishzz.json"
```

## 🧥 Import configured profiles
With the arrival of v1.5 it is no longer necessary to import all the profiles with their respective variants, you will choose the configuration, for this you can redirect to the following script and this script will take you to choose the configurations

If you have the luxury of having the possibility to use Web-Request you can use the following command
```batch
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest -Uri "https://github.com/Matishzz/OBS-Studio/releases/download/v1.5/CreateProfile.bat" -OutFile "$env:TEMP\CreateProfile.bat"; Start-Process -FilePath "$env:TEMP\CreateProfile.bat"
```
If it doesn't work you can download and run it [Download here](https://github.com/Matishzz/TESTT3/releases/download/v1.5/CreateProfile.bat)

## 📝 Import theme 
Previously we used a theme that today is no longer possible to use because they were limited `.qss` (QT style sheets) which are an extended version of the web CSS relatively recently changed to even more extended files called `OBT/OVT`, taking into account this there is no other possibility but to update and leave aside the old theme we had that was so beautiful but I found this called <a href="https://obsproject.com/forum/resources/fluent-dark-grey.1961/">Fluent Dark (Grey)</a> which is quite similar and I quite like, taking into account that this is putting into play a subjective opinion you can browse <a href="https://obsproject.com/forum/resources/categories/themes.10/">themes\resources</a> and download the Theme that you like. 

If you want to import it from Web-Request you can do it with the following command
```batch
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest -Uri 'https://obsproject.com/forum/resources/fluent-dark-grey.1961/download' -OutFile $env:TEMP\theme.zip; Expand-Archive -Path $env:TEMP\theme.zip -DestinationPath $env:ProgramFiles\obs-studio\data\obs-studio\themes -Force"
```

If you want to import it manually, you will have to download the file from Themes <a href="https://obsproject.com/forum/resources/fluent-dark-grey.1961/">Fluent Dark (Grey)</a>, then unzip it and move the content inside to <code>%appdata%\obs-studio\themes</code>.

<br>

<p align="center">
  <a href="https://twitter.com/Matishzz">
    <img src="https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter" alt="Twitter">
  </a>
  <a href="https://discord.io/MatishzzTweaking">
    <img src="https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord" alt="Discord">
  </a>
</p>
