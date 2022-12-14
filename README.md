<p align="center">

  <img src="https://jdleongomez.info/es/post/obs/featured.png" height="100" />
</p>


## Configuration and application of profiles for OBS Studio

This batch was made for people who play and want to make video broadcasts, record or take clips without any interruption within their game, for that I have created this batch that downloads OBS Studio, Configure according to your graphics and leave everything ready.

For this batch to work you need to put the whole Installation command in CMD, if you are using __Powershell 2.0__ you will not be able to use it because there is no WebRequest or DownloadFile, which is the way it uses to download the necessary files.

### Installation 🤖
To run this script it is as simple as opening the CMD and the following:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/Matishzz/OBS-Studio/releases/download/Complements/OBS.Studio.US.bat" -OutFile "$env:temp\OBS.bat"; Start-process $env:temp\OBS.bat
```

### Installing Manually 🔧
For manual installation and configuration we will have to install [OBS Studio](https://obsproject.com/es/download) and perform the following steps after the installation of OBS and run it only once 
We will download the necessary complements:

* [AppdataAMDOBS](https://github.com/Matishzz/OBS-Studio/releases/download/Complements/AppdataAMDOBS.zip) Everything inside will be replaced in %appdata%\obs-studio
* [AppdataNvidiaOBS](https://github.com/Matishzz/OBS-Studio/releases/download/Complements/AppdataNvidaOBS.zip) Everything inside will be replaced in %appdata%\obs-studio
* [ProgramFilesOBS](https://github.com/Matishzz/OBS-Studio/releases/download/Complements/ProgramFileOBS.zip) Everything inside will be replaced in %programfiles%\obs-studio\data\obs-studio

### Custom LUTs filters created by [Gaming Careers](https://www.youtube.com/channel/UClx4eJ_EP9MJdz19JUjKD1w) & [Jordan Wages](https://obsproject.com/forum/threads/free-lut-filter-pack.78307/#post-330293) 🎲
Download and apply LUTs Customs filters for the camera:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/Matishzz/OBS-Studio/releases/download/Complements/InstallLUTs.bat" -OutFile "$env:temp\InstallLUTs.bat"; Start-process $env:temp\InstallLUTs.bat.bat
```

### ReplayBuffer AutoStart 🔗
For OBS Studio ReplayBuffer to start automatically when you turn on your PC you will have to run this script via CMD:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/Matishzz/OBS-Studio/releases/download/Complements/ReplayBuffer.bat" -OutFile '%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\ReplayBuffer.bat'
```

* __Thank you very much [Couleur](https://twitter.com/CouleurMinemen) for helping me in the creation of this script__

[![Twitter](https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter)](https://twitter.com/Matishzz)
[![Discord](https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord)](https://discord.io/MatishzzTweaking)

