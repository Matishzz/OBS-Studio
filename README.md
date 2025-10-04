<div align="center">
  <img src="https://jdleongomez.info/es/post/obs/featured.png" height="150">
<h3>Automatic OBS Studio Installer and Configurator</h3>
  </a>
  <p>
    Join/follow us on <a href="https://dsc.gg/matishzz-tweak" target="_blank">Discord</a> | <a href="https://x.com/Matishzz" target="_blank">𝕏 (Twitter)</a>
  </p>
  <p>
    <a href="https://github.com/Matishzz/OBS-Studio/blob/main/Installation%20manual.md">Installation Manual</a> ⠂<a href="https://github.com/Matishzz/OBS-Studio/blob/main/Troubleshooting.md">Troubleshooting</a> ⠂ <a href="https://github.com/Matishzz/OBS-Studio/blob/main/AMF%20Options.md">AMF Options</a>
    
  </p>
</div>

---

<p align="center">
This project started on <b>August 3, 2021</b>, with the main objective to help those who had no idea or time to properly configure OBS Studio. 
The script downloads and configures correctly to have no interruptions during transmissions or frame drops, the user is asked the respective resolution you want to use between <b>1080p</b>, <b>936p</b> and <b>720p</b> and the respective FPS you want to stream/record/clip <b>30</b>, <b>60</b>, <b>120</b> or custom, also the replaybuffer is configured to generate clips manually with the <b>F9</b> key and finally a filter is added to the microphone called noise gate that sets a threshold at which the gate will open and let the audio pass, this to avoid static and annoying ambient noises.
</p>

<br>

🚀 Automatic installation
---------------
Run the following command in CMD:

```batch
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest -Uri "https://github.com/Matishzz/OBS-Studio/releases/download/v1.5/OBS.Studio.1.5.bat" -OutFile "$env:TEMP\OBS.Studio.1.5.bat"; Start-Process -FilePath "$env:TEMP\OBS.Studio.1.5.bat"
```

🔗 ReplayBuffer Startup
---------------
Run the following command in CMD:
```batch
reg add "HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\Run" /v "obs64" /t REG_SZ /d "cmd.exe /c del \"%appdata%\obs-studio\.sentinel\" /f /q && start \"\" /d \"C:\Program Files\obs-studio\bin\64bit\" obs64.exe --startreplaybuffer --minimize-to-tray" /f
```
> [!NOTE]  
> Since the `--disable-shutdown-check` flag has been removed for 32.0, the solution I found was to force the deletion of the `.sentinel` folder.

If you want to add more specific parameters you can consult <a href="https://obsproject.com/kb/launch-parameters">launch-parameters</a>


📜 Objectives for OBS Studio v1.8
---------------

```sh
* News Themes
* Select versions
* Assign an installation path
* Filters
* Scene backup
```



