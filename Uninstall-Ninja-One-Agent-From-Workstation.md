## Uninstall Ninja One RMM Agent from Windows WOrkstation

Use the steps below only for cases in which the agent has not reported in and/or the install is corrupt.

#### Following command can be used to uninstall Ninja silently **if you do not have uninstall prevention enabled:**

```
"C:\Program Files (x86)\<NinjaInstallFolder>\uninstall.exe" --mode unattended
```

#### If you **do have uninstall prevention enabled,** please follow these steps:


1. Make sure that the NinjaRMMAgent service is running on the device.
2. Run "C:\Program Files (x86)\<NinjaInstallFolder>\NinjaRMMAgent.exe" -disableUninstallPrevention  


*This will restore the agent uninstaller for that device.*


Run "C:\Program Files (x86)\<NinjaInstallFolder>\uninstall.exe" --mode unattended
To ensure complete removal, check for and delete the following folders:

C:\Program Files (x86)\<OrganizationName-Version>\
C:\ProgramData\NinjaRMMAgent\
Note that there may be multiple folders for the Ninja install directory found in Program Files (x86) and it is important to remove all of them.

Alternatively, you can use the PowerShell script (titled NewAgentRemoval_2022) that is linked as an attachment at the end of this article. Please note, the script must be run as administrator. Additionally, one or more of the following parameters must be used with this script:

