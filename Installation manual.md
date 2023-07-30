<p align="center"> <img src="https://jdleongomez.info/es/post/obs/featured.png" height="100" /> </p>

##  <p align="center"> Manual procedure for the correct installation and configuration of OBS Studio </p>

---
<br>

## 🔗 Installation of OBS Studio
This step is very simple, the only thing we have to do is to download the installer of the [latest version of OBS Studio](https://obsproject.com/es/download) and run it 

## 📌 Running OBS Studio for the first time
When OBS Studio is run for the first time, a folder is created in `%appdata%` which stores the OBS Studio configuration, the strategy I take to import the profiles is to create the `.ini` and `.json` that save the configuration, we can manually open OBS and close it or run this command in CMD
```sh
cd %programfiles%\obs-studio\bin\64bit & powershell Start-Process -FilePath "obs64.exe" -WindowStyle Minimized & timeout /t 3 >nul & powershell stop-process -ProcessName obs64 -Force
```

## 🎈 Configure Global.ini
As its name says, this section keeps the global configuration of OBS Studio, this configuration is stored in `%appdata%\OBS Studio` and keeps settings such as the current theme, the proportions of the docks among other things, to run the bath that makes this procedure is necessary to first download and run it. 
* [Download here](https://github.com/Matishzz/OBS-Studio/releases/download/v1-Manual/Global.bat)

## 🔌 Create Scene
The `global.ini` is configured so that the scene present is for the `matishzz.json` scene, for this run this batch, this configuration brings a filter for the microphone among other things.
* [Download here](https://github.com/Matishzz/OBS-Studio/releases/download/v1-Manual/CreateScene.bat)

## 🔒 Create Default Profile
The `global.ini` is configured so that the default profile is in the `Default @Matishzz`, for this run this batch, this can be skipped without any problem
* [Download here](https://github.com/Matishzz/OBS-Studio/releases/download/v1-Manual/CreateDefault.bat)

## 🧥 Import configured profiles
To import the profiles we will run the batch of our respective graphics card, if you have problems with the detection of the graphics in the automatic batch here you have to run the batch of your dedicated card but I recommend you to disable it, it is also useful if you do not want to uninstall your current OBS and want to test the configuration. 
- ### NVIDIA Profiles 🟢
  - To import the OBS Studio configuration for the NVIDIA graphics card you have to run the following batch and wait for it to finish, when it finishes you will have your configuration imported.
      * [Download here](https://github.com/Matishzz/OBS-Studio/releases/download/v1-Manual/CreateProfilesNVIDIA.bat)

- ### AMD Profiles 🔴
   - To import the OBS Studio configuration for the AMD graphics card you have to run the following batch and wait for it to finish, when it finishes you will have your configuration imported.
       * [Download here](https://github.com/Matishzz/OBS-Studio/releases/download/v1-Manual/CreateProfilesAMD.bat)

## 📝 Import theme 
To import the theme from obs you have to download the theme and drag it to `"%programfiles%\obs-studio\data\obs-studio\themes`, the automatic script imports the [Moonlight theme](https://github.com/WyzzyMoon/Moonlight/releases/tag/v1.0), but you can see more at [here](https://obsproject.com/forum/resources/categories/themes.10/).

<br>

<p align="center">
  <a href="https://twitter.com/Matishzz">
    <img src="https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter" alt="Twitter">
  </a>
  <a href="https://discord.io/MatishzzTweaking">
    <img src="https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord" alt="Discord">
  </a>
</p>
