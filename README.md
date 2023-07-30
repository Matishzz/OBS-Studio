<p align="center">

  <img src="https://jdleongomez.info/es/post/obs/featured.png" height="100" />
</p>

<p align="center"> <a href="https://github.com/Matishzz/OBS-Studio/blob/main/Installation%20manual.md">Installation manual</a> ⠂ <a href="https://github.com/Matishzz/OBS-Studio/blob/main/Troubleshooting.md">Troubleshooting</a> </p>

<p align="center">
This batch was made for people who play games and want to make video transmissions, record or take clips without any interruption inside their game, for that I created this batch that downloads OBS Studio, configures it according to your graphics and leaves everything ready.
</p>

<p align="center">
The Invoke-WebRequest is used from Powershell 3.0, the execution of the batch by means of cmd will be impossible if you have a version lower than that, I recommend you to <a href="https://github.com/Matishzz/OBS-Studio/releases/download/v1.0/OBS.Studio.v1.0.bat">Download</a> and install the batch. 
</p>
<br>

### Automatic installation 🤖
For the automatic installation all you have to do is execute this command in CMD and the script will start running
```ruby
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest -Uri "https://github.com/Matishzz/OBS-Studio/releases/download/v1.0/OBS.Studio.v1.0.bat" -OutFile "$env:TEMP\OBS.Studio.v1.0.bat"; Start-Process -FilePath "$env:TEMP\OBS.Studio.v1.0.bat"
```

<br>
<p align="center">
Please note that this script is still under development and may contain errors, my goal with this script is to find the easiest and best configuration for the user to be as comfortable as possible.
</p>

<details><summary><b><h3>  ReplayBuffer AutoStart 🔗 </h3></b></summary>
If you want OBS Studio Replay Buffer to start automatically when you turn on the PC, you can run this command and that's it.
  
```ruby
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/Matishzz/OBS-Studio/releases/download/v1.0/ReplayBuffer.bat" -OutFile '%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\ReplayBuffer.bat'
```
If you have problems running it, you can download the [ReplayBuffer.bat](https://github.com/Matishzz/OBS-Studio/releases/download/v1.0/ReplayBuffer.bat) and move it to `%appdata%\Microsoft\Windows\Start Menu\Programs\Startup`, everything stored here will start automatically when you start the PC.
If you want to remove it put this in CMD

```ruby
powershell Remove-Item -path '%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\ReplayBuffer.bat'
```

</details>

<br>

<p align="center">
  <a href="https://twitter.com/Matishzz">
    <img src="https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter" alt="Twitter">
  </a>
  <a href="https://discord.io/MatishzzTweaking">
    <img src="https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord" alt="Discord">
  </a>
</p>


