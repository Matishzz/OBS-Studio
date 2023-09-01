<p align="center">

  <img src="https://jdleongomez.info/es/post/obs/featured.png" height="100">
  
  <h3 align="center">Automatic OBS Studio Installer and Configurator</h3>
  
<p align="center">
<a href="https://github.com/Matishzz/OBS-Studio/blob/main/Installation%20manual.md">Installation manual</a>
⠂ 
<a href="https://github.com/Matishzz/OBS-Studio/blob/main/Troubleshooting.md">Troubleshooting</a> 

</p>

---------------
<p align="center">
This project started on August 3, 2021, with the main objective to help those who had no idea or time to properly configure OBS Studio. 
The script downloads and configures correctly to not have interruptions during transmissions or frame drops, 6 profiles are applied which you can apply for different streaming/recording qualities, which are 1080p, 936p and 720p in its two variations of fps 30 and 60, also the replaybuffer is configured to generate clips manually with the F9 key and finally a filter is added to the microphone called noise gate which sets a threshold at which the gate will open and let the audio through, this to avoid static and annoying ambient noises.
</p>

<br>

🚀 Automatic installation
---------------
Run the following command in CMD:
```ruby
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest -Uri "https://github.com/Matishzz/OBS-Studio/releases/download/v1.0/OBS.Studio.v1.0.bat" -OutFile "$env:TEMP\OBS.Studio.v1.0.bat"; Start-Process -FilePath "$env:TEMP\OBS.Studio.v1.0.bat"
```

<details>
<summary> <h3>🔗 AutoStart ReplayBuffer </h3> </summary>
The ReplayBuffer is the best option compared to all competing applications, but for ReplayBuffer to work it has to be run from OBS Studio or open OBS Studio with a parameter called `--startreplaybuffer`. That is our strategy to run it at startup, this script imports a `.bat` in shell:startup which opens OBS Studio with this parameter so that after windows starts OBS Studio runs with ReplayBuffer activated and ready for you to take clips.


Run the following command in CMD:
```ruby
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/Matishzz/OBS-Studio/releases/download/v1.0/ReplayBuffer.bat" -OutFile '%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\ReplayBuffer.bat'
```
<br> 

If you want to remove it put this in CMD
```ruby
del "%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\ReplayBuffer.bat"
```

 <h3 align="center"> :exclamation: If you experience problems running the script, you should manually move the <a href="https://github.com/Matishzz/OBS-Studio/releases/download/v1.0/ReplayBuffer.bat">Replaybuffer.bat</a> to shell:startup (Win + R > shell:startup) :exclamation: </h3>

<hr>
</details>

📜 Objectives for OBS Studio v1.5
---------------

```sh
* News Themes
* Intel HD Graphics support 
* Fixing bugs
* Assign an installation path
```


❔ What's behind the script
---------------
<a href="https://chocolatey.org/">Chocolatey</a> is used for the installation of OBS Studio, then the GPU is identified if it is AMD or NVIDIA, then the profiles folder is created which contains ``basic.ini`` that stores the configuration is written with the configuration without using dependencies nor anything outside of Powershell 2.0 and CMD, after creating the 6 profiles with their 2 variants, the <a href="https://github.com/WyzzyMoon/Moonlight/releases/tag/v1.0">Mooonlight</a> theme is imported using Invoke-WebRequest

<p align="center">
  <a href="https://twitter.com/Matishzz">
    <img src="https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter" alt="Twitter">
  </a>
  <a href="https://discord.io/MatishzzTweaking">
    <img src="https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord" alt="Discord">
  </a>
</p>


