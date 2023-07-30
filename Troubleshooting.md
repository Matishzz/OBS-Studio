<p align="center">

  <img src="https://jdleongomez.info/es/post/obs/featured.png" height="100" />
</p>

<table>
<tr>
<td>
This is the troubleshooting section if you have been redirected here you may have experienced an error during scripting 
</td>
</tr>
</table>

When using this Bath you may experience problems due to several things, this project is still under development so there may still be some problems or bugs, here is a list of some of the problems and their solutions

<details><summary><b><h3> There was an error during the installation of Chocolatey ❗ </h3></b></summary>

Chocolatey will not install if you have a build lower than w10 2003, w7 will work Server core too but not Windows Nano Server.
If you have all the requirements and you still have problems to install Chocolatey, it may be that the powershell execution policy for the user interferes with the execution of the script, run this command in powershell to allow any script to run without restrictions 
```sh
Set-ExecutionPolicy Bypass -Scope CurrentUser -Force
```
</details>

---

<details><summary><b><h3> For now the script doesn't support Intel UHD Graphics ❗ </h3></b></summary>
For now the script does not have profiles for intel integrated graphics, if you have a dedicated graphics and you still have this sign you may have to disable the integrated in BIOS, the steps to do it may vary depending on the motherboard we have, for example in my case is 
‎<br>
<br>
  
```sh
* IO Ports
  * Initial Display Output > PCIe 1 Slot
  * Integrated Graphics > Disabled
    * F10 > OK
```


</details>

---

<details>
  <summary><b><h3> Apparently there was an error when importing the Theme Moonlight ❗ </h3></b></summary>
  
  In this section to install the Moonlight theme is installed with an Invoke-WebRequest, if you use a version prior to Powershell 3.0 you can not use this command. If you want to install the Moonlight theme, you can also go directly to the [Moonlight Github](https://github.com/WyzzyMoon/Moonlight/releases/tag/v1.0) of the creator and download it from there. Then, you have to unzip it to `%programfiles%\obs-studio\data\obs-studio\themes`.
  
</details>

---

<details>
  <summary><b><h3> It has been detected that OBS Studio is still installed ❗ </h3></b></summary>
  
  The solution may be quite obvious, it may be as simple as uninstalling OBS Studio from Control Panel, but some users experience an error when uninstalling OBS, that a folder called OBS-Studio is kept in programfiles, the script automatically detects this folder and produces this error, to fix it is as simple as deleting it manually by going to `%programfiles%` or putting this command in cmd
  ```sh
  rmdir /s /q "%programfiles%\obs-studio"
  ```

</details>

---

<details>
  <summary><b><h3> Here was an error during the installation of OBS Studio ❗ </h3></b></summary>
  
  This solution may be because Chocolatey detects that OBS-Studio is installed, to solve this problem we will have to put in the CMD this command and restart the PC
  ```sh
  choco uninstall obs-studio -y --force
  ```

</details>

---

<br>
<p align="center"> Some errors may start to appear over time because these are some errors that I was able to collect, if you experience any errors that are not on the list or if you are still having issues even though you have done the troubleshooting contact me via Twitter. </p>

<p align="center">
  <a href="https://twitter.com/Matishzz">
    <img src="https://img.shields.io/badge/-Twitter-black?style=for-the-badge&logo=twitter" alt="Twitter">
  </a>
  <a href="https://discord.io/MatishzzTweaking">
    <img src="https://img.shields.io/badge/-Discord-black?style=for-the-badge&logo=discord" alt="Discord">
  </a>
</p>
