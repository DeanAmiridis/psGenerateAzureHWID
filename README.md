# psGenerateAzureHWID
This is a simple UI tool that follows the `official microsoft manual process` to generate the AzureHWID CSV on workstations (shown below).
_Rather the HWID directory be made, it generates the AutopilotHWID.csv in the location of the exe._

```
New-Item -Type Directory -Path "C:\HWID"
Set-Location -Path "C:\HWID"
$env:Path += ";C:\Program Files\WindowsPowerShell\Scripts"
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
Install-Script -Name Get-WindowsAutopilotInfo
Get-WindowsAutopilotInfo -OutputFile AutopilotHWID.csv
```
## UI:
![psGenerateAzureHWID](http://aselectfew.com/img/psGenerateAzureHWID.png)

## Usage:
1) Download file from releases page (here)
2) Run EXE `as administrator/elevated permissions`
3) Press "Generate"
That's it!
