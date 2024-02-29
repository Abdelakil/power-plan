
# fix low frequency stuck in asus tuf15 gaming on battery



## 1. disable modern standby
in cmd:
```
reg add HKLM\System\CurrentControlSet\Control\Power /v PlatformAoAcOverride /t REG_DWORD /d 0
```

to enable it again (if you need to):
```
reg delete "HKLM\System\CurrentControlSet\Control\Power" /v PlatformAoAcOverride /f
``` 


## 2. Add and enable it ultimate performance power plan
in cmd:
```
powercfg -duplicatescheme e9a42b02-d5df-448d-aa00-03f14749eb61
```

now go choose the powerplan in :
Control Panel\Hardware and Sound\Power Options


## 3. Editing the power plan
Click on change plan settings, then click on change advanced power settings.
Now click on processor power management, and modify minimun power state to 10% or higher and maximum power state to 85% or lower (to avoid overheating when playing).
