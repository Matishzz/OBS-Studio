## Configuration and application of profiles for OBS Studio

This batch was made for people who play and want to make video broadcasts, record or take clips without any interruption within their game, for that I have created this batch that downloads OBS Studio, Configure according to your graphics and leave everything ready.

_For this batch to work you need to put the whole Installation command in CMD, if you are using __Powershell 2.0__ you will not be able to use it because there is no WebRequest or DownloadFile, which is the way it uses to download the necessary files._

#### Installation (In CMD) 🤖
To run this script it is as simple as opening the CMD and the following:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/Matishzz/OBS-Studio/releases/download/Complements/OBS.Studio.US.bat" -OutFile "$env:temp\OBS.bat"; Start-process $env:temp\OBS.bat
```

#### Installing Manually 🔧
For manual installation and configuration we will have to install OBS Studio and perform the following steps after the installation of OBS and run it only once 
We will download the necessary complements:
> [AppdataAMDOBS](https://github.com/Matishzz/OBS-Studio/releases/download/Complements/AppdataAMDOBS.zip) Everything inside will be replaced in %appdata%\obs-studio
> [AppdataNvidiaOBS](https://github.com/Matishzz/OBS-Studio/releases/download/Complements/AppdataNvidaOBS.zip) Everything inside will be replaced in %appdata%\obs-studio
> [ProgramFilesOBS](https://github.com/Matishzz/OBS-Studio/releases/download/Complements/ProgramFileOBS.zip) Everything inside will be replaced in %programfiles%\obs-studio\data\obs-studio

##### ReplayBuffer AutoStart 🔗
For OBS Studio ReplayBuffer to start automatically when you turn on your PC you will have to run this script via CMD:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/Matishzz/OBS-Studio/releases/download/Complements/ReplayBuffer.bat" -OutFile '%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\ReplayBuffer.bat'

* Thank you very much [Couleur](https://twitter.com/CouleurMinemen) for helping me in the creation of this script
