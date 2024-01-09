# PowerShell Cheat-Sheet

## File Management

| Command | Description |
| --- | --- |
| `Get-ChildItem` | List files and directories |
| `Get-Content <file>` | Get the content of a file |
| `Set-Content <file> <content>` | Set the content of a file |
| `New-Item <file>` | Create a new file |
| `New-Item <directory> -ItemType Directory` | Create a new directory |
| `Remove-Item <file>` | Remove a file |
| `Remove-Item <directory> -Recurse` | Remove a directory |
| `Rename-Item <file> <new_file>` | Rename a file or directory |
| `Copy-Item SOURCE DEST` | Copy a file |
| `Copy-Item SOURCE DEST -Recurse` | Copy a directory |
| `Move-Item SOURCE DEST` | Move a file or directory |

## Process Management

| Command | Description |
| --- | --- |
| `Get-Process` | List running processes |
| `Stop-Process -Name <process>` | Stop a process |
| `Start-Process <process>` | Start a new process |
| `Wait-Process -Name <process>` | Wait for a process to finish |

## Service Management

| Command | Description |
| --- | --- |
| `Get-Service` | List services |
| `Start-Service <service>` | Start a service |
| `Stop-Service <service>` | Stop a service |
| `Restart-Service <service>` | Restart a service |
| `Set-Service <service> -StartupType Automatic` | Set a service to start automatically |
| `Set-Service <service> -StartupType Manual` | Set a service to start manually |
| `Set-Service <service> -StartupType Disabled` | Disable a service |

## User Management

| Command | Description |
| --- | --- |
| `Get-LocalUser` | List local users |
| `New-LocalUser <user>` | Create a new local user |
| `Remove-LocalUser <user>` | Remove a local user |
| `Set-LocalUser <user> -Password <password>` | Set the password for a local user |
| `Add-LocalGroupMember -Group Administrators -Member <user>` | Add a user to the Administrators group |
| `Remove-LocalGroupMember -Group Administrators -Member <user>` | Remove a user from the Administrators group |

## Network Management

| Command | Description |
| --- | --- |
| `Get-NetIPAddress` | List IP addresses |
| `Get-NetAdapter` | List network adapters |

## Windows Updates

| Command | Description |
| --- | --- |
| `Install-Module -Name PSWindowsUpdate` | Install the PSWindowsUpdate module |
| `Get-Command -Module PSWindowsUpdate` | List all commands in the PSWindowsUpdate module |
| `Get-WUInstall` | Install Windows updates |

## Windows Features

| Command | Description |
| --- | --- |
| `Get-WindowsFeature` | List Windows features |
| `Install-WindowsFeature <feature>` | Install a Windows feature |
| `Uninstall-WindowsFeature <feature>` | Uninstall a Windows feature |

## Connect to a remote computer

| Command | Description |
| --- | --- |
| `Enter-PSSession -ComputerName <name> -Credential <user>` | Open a new remote session |
| `Exit-PSSession` | Close the current remote session |
| `Invoke-Command -ComputerName <name> -ScriptBlock { <command> }` | Run a command on a remote computer |
| `Invoke-Command -ComputerName <name> -FilePath <script>` | Run a script on a remote computer |
PowerShell is a task automation and configuration management program from Microsoft, consisting of a command-line shell and the associated scripting language.

## Install PowerShell
PowerShell was made open-source and cross-platform with PowerShell Core, and can be installed on multiple operating systems.

### Windows
1. Download MSI Package from the [Official PowerShell Docs](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.2)
2. Set up PowerShell Profile in Windows Terminal ([[windows-terminal]]).
```json
"commandline": "pwsh.exe -nologo",
"name": "Powershell",
"source": "Windows.Terminal.PowershellCore"
```

### Linux (Ubuntu)
```sh
# Update the list of packages
sudo apt-get update
# Install pre-requisite packages.
sudo apt-get install -y wget apt-transport-https software-properties-common
# Download the Microsoft repository GPG keys
wget -q https://packages.microsoft.com/config/ubuntu/20.04/packages-microsoft-prod.deb
# Register the Microsoft repository GPG keys
sudo dpkg -i packages-microsoft-prod.deb
# Update the list of packages after we added packages.microsoft.com
sudo apt-get update
# Install PowerShell
sudo apt-get install -y powershell
# Start PowerShell
pwsh
```

## Profile
Set up a PowerShell Profile by opening the profile script :
```powershell
code $PROFILE
```

## (Optional) Set up starship Prompt
You can customize the look and feel of PowerShell with the Starship Prompt ([[starship]]).


#### Useful commands:
Find string in files

```powershell
Get-ChildItem -Recurse | Select-String "search-string" -List | Select Path

%% For example %%

Get-ChildItem `
        -Path "C:\data\path" -Filter "Example*.dat" -recurse | `
    Select-String -pattern "dummy" | `
    Select-Object -Property Path,LineNumber,Line | `
    Export-CSV "C:\ResultFile.csv"


Get-ChildItem -Recurse *.java | Select-String "dummy" -List | Select Path
```

```powershell
ls -r | ?{ $_ | Select-String -Pattern "search-string" }
```
