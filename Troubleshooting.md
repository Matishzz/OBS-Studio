<p align="center">

  <img src="https://jdleongomez.info/es/post/obs/featured.png" height="100" />

  <h3 align="center">Troubleshooting section for v1.25</h3>
<br>

<p align="center">
I have fixed most of the errors of v1, but in a context like this anomalies can appear everywhere, I am still in process so that most people can run my script quickly, easily and without having to resort to a guide to solve your problem, if you find any unlisted error please contact me so I will get to work to fix it as soon as possible and the same if any of these solutions was not useful to you. (v1.25 is still a beta version, if you are using v1 redirect to the <a href="https://github.com/Matishzz/OBS-Studio/blob/main/Basement/Troubleshooting%20for%20v1.md">Troubleshooting section for v1 </a> )  </p>

⚠️ OBS Studio has been detected installed [ERROR 125] ⚠️
----
This error is because it has been detected that OBS Studio is installed and the script does not allow it, if you have installed OBS Studio be sure to uninstall it, if the problem persists even after uninstalling it may be because chocolatey still detects that it is installed and throws the error as my way to check if it is installed is through a `choco list`, use the following command and restart the PC to continue with the script
```ruby
choco uninstall obs-studio
```

⚠️ A folder called OBS-Studio has been detected in %programfiles% [ERROR 150] ⚠️
----
There are times when you uninstall OBS Studio but the folder located in "C:\Program Files" is not deleted, the script detects if this folder exists in that directory and if it recognizes it throws this error, try to delete it, to do this you can go to the folder manually and delete it or run the following command in **CMD**
```ruby
rd /s /q "%programfiles%\obs-studio"
```

⚠️ There was an error during the installation of Chocolatey [ERROR 200] ⚠️
----
Chocolatey will not install if you have a build lower than w10 2003, w7 will work Server core as well but not Windows Nano Server. If you have all the requirements and still have problems installing Chocolatey, it may be that the powershell execution policy for the user interferes with the execution of the script, run this command in powershell to allow any script to run without restrictions, to fix this run the following command from **Powershell**
```ruby
Set-ExecutionPolicy Bypass -Scope CurrentUser -Force
```

⚠️ Apparently there was an error when importing the Theme Moonlight [ERROR 300] ⚠️
----
There may be some anomaly when importing the theme, you can import the theme manually by following the steps at [Import-theme](https://github.com/Matishzz/OBS-Studio/blob/main/Installation%20manual.md#-import-configured-profiles).

<br>

<p align="center">
  <a href="https://twitter.com/Matishzz">
    <img src="https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter" alt="Twitter">
  </a>
  <a href="https://discord.io/MatishzzTweaking">
    <img src="https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord" alt="Discord">
  </a>
</p>
