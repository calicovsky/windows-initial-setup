# Windows Initial Setup

1. Swap the Caps Lock key with the ‘No Convert’ key.

Launch Command Prompt as administrator and

```
REG ADD "HKLM\SYSTEM\CurrentControlSet\Control\Keyboard Layout" /v "Scancode Map" /t REG_BINARY /d 00000000000000004000000038007b007b003a002a00730000000000
```

2. Install WSL2

3. Install Chocolatey and install core applications

Again, launch Command Prompt as administrator, then

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "[System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"

choco install microsoft-windows-terminal autohotkey firefox googlechrome brave git python 7zip vscode notepadplusplus
```

4. Install monospace fonts for command prompts
