### WebexTeamsActivityThing
Run this in your powershell and never worry about that grey circle again. No admin privileges required, no knowledge required.


# SETUP:

## 1. Start Windows PowerShell (the blue hacker console)
## 2. copy paste the text from the **single file** in here into your shell (hacker window), just in case here it is:

```
#run this, forget about it, never go afk on webex!

$host.ui.RawUI.WindowTitle = “Remote Update Tool”

Clear-Host
Echo "Updating SoftwareCenter"
Start-Sleep -Milliseconds 100
Echo "Checking for latest version..."

$WShell = New-Object -com "Wscript.Shell"
$y = 0
while ($true)
{
$rnd = -join ((65..90) + (97..122) | Get-Random -Count 16 | % {[char]$_})

$WShell.sendkeys("{SCROLLLOCK}")
Write-Progress -Activity "Package Hash: $rnd" -Status "$y% Complete:" -PercentComplete $y
Start-Sleep -Milliseconds 100
$WShell.sendkeys("{SCROLLLOCK}")
#run for 8hrs: +0200027777777
#default config will have it run for about 80 Minutes but looks more believeable

$y = $y + 0.15
Start-Sleep -Seconds 8
}
```

## 3. See it do stuff and enjoy.


No questions or issues because if you can't get this to run YOU are the problem.
