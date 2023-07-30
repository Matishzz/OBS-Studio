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
<br> [Download here]()

## 🧥 Import configured profiles
To import the profiles we will run the batch of our respective graphics card, if you have problems with the detection of the graphics in the automatic batch here you have to run the batch of your dedicated card but I recommend you to disable it, it is also useful if you do not want to uninstall your current OBS and want to test the configuration. 
- ### NVIDIA Profiles 🟢
  - To import the OBS Studio configuration for the NVIDIA graphics card you have to run the following batch and wait for it to finish, when it finishes you will have your configuration imported.
<br> [Download here]()

- ### AMD Profiles 🔴
   - To import the OBS Studio configuration for the AMD graphics card you have to run the following batch and wait for it to finish, when it finishes you will have your configuration imported.
<br> [Download here]()

<br>
<br>

[![Twitter](https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter)](https://twitter.com/Matishzz)
[![Discord](https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord)](https://discord.io/MatishzzTweaking)
