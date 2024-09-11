## To create encode base 64 for powershell code steps are :
$scriptPath = "C:\path\to\your\script.ps1"

$bytes = [System.Text.Encoding]::Unicode.GetBytes((Get-Content -Path $scriptPath -Raw))

$encodedScript = [Convert]::ToBase64String($bytes)

$encodedScript | Out-File "C:\path\to\save\encoded_script.txt"

## Save Encode base 64 in ps1 as :

$encodedScript = "YOUR_BASE64_STRING_HERE"

$scriptBytes = [System.Convert]::FromBase64String($encodedScript)
$decodedScript = [System.Text.Encoding]::Unicode.GetString($scriptBytes)

Invoke-Expression $decodedScript



--------------------------------------------------------------------------------------------------------------

# PowerShell Script to EXE Conversion

## Installation
Install-Module -Name ps2exe -Force

Install-Module -Name ps2exe -Force -Scope CurrentUser

## To Run
Invoke-ps2exe "C:\Path\To\YourScript.ps1" "C:\Path\To\YourScript.exe"
