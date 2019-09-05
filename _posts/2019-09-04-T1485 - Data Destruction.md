---
published: true
title: T1485 Data Destruction
---
## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1485)
<blockquote>Adversaries may destroy data data and files on specific systems or in large numbers on a network to interrupt availability to systems, services, and network resources. Data destruction is likely to render stored data irrecoverable by forensic techniques through overwriting files or data on local and remote drives.(Citation: Symantec Shamoon 2012)(Citation: FireEye Shamoon Nov 2016)(Citation: Palo Alto Shamoon Nov 2016)(Citation: Kaspersky StoneDrill 2017)(Citation: Unit 42 Shamoon3 2018)(Citation: Talos Olympic Destroyer 2018) Common operating system file deletion commands such as <code>del</code> and <code>rm</code> often only remove pointers to files without wiping the contents of the files themselves, making the files recoverable by proper forensic methodology. This behavior is distinct from <a href="https://attack.mitre.org/techniques/T1488">Disk Content Wipe</a> and <a href="https://attack.mitre.org/techniques/T1487">Disk Structure Wipe</a> because individual files are destroyed rather than sections of a storage disk or the disk's logical structure.
<br/>
<br/>
Adversaries may attempt to overwrite files and directories with randomly generated data to make it irrecoverable.(Citation: Kaspersky StoneDrill 2017)(Citation: Unit 42 Shamoon3 2018) In some cases politically oriented image files have been used to overwrite data.(Citation: FireEye Shamoon Nov 2016)(Citation: Palo Alto Shamoon Nov 2016)(Citation: Kaspersky StoneDrill 2017)
<br/>
<br/>
To maximize impact on the target organization in operations where network-wide availability interruption is the goal, malware designed for destroying data may have worm-like features to propagate across a network by leveraging additional techniques like <a href="https://attack.mitre.org/techniques/T1078">Valid Accounts</a>, <a href="https://attack.mitre.org/techniques/T1003">Credential Dumping</a>, and <a href="https://attack.mitre.org/techniques/T1077"> Windows Admin Shares </a>.(Citation: Symantec Shamoon 2012)(Citation: FireEye Shamoon Nov 2016)(Citation: Palo Alto Shamoon Nov 2016)(Citation: Kaspersky StoneDrill 2017)(Citation: Talos Olympic Destroyer 2018)</blockquote>

## Atomic Tests

- Atomic Test #1 - Windows - Delete Volume Shadow Copies

- Atomic Test #2 - Windows - Delete Windows Backup Catalog

- Atomic Test #3 - Windows - Disable Windows Recovery Console Repair

- Atomic Test #4 - Windows - Overwrite file with Sysinternals SDelete

<br/>

## Atomic Test #1 - Windows - Delete Volume Shadow Copies
Deletes Windows Volume Shadow Copies. This technique is used by numerous ransomware families and APT malware such as Olympic Destroyer.

**Supported Platforms:** Windows


#### Run it with `command_prompt`!  Elevation Required (e.g. root or admin) 

```
vssadmin.exe delete shadows /all /quiet
```

<br/>
<br/>

## Atomic Test #2 - Windows - Delete Windows Backup Catalog
Deletes Windows Backup Catalog. This technique is used by numerous ransomware families and APT malware such as Olympic Destroyer.

**Supported Platforms:** Windows


#### Run it with `command_prompt`!  Elevation Required (e.g. root or admin) 

```
wbadmin.exe delete catalog -quiet
```

<br/>
<br/>

## Atomic Test #3 - Windows - Disable Windows Recovery Console Repair
Disables repair by the Windows Recovery Console on boot. 
This technique is used by numerous ransomware families and APT malware such as Olympic Destroyer.

**Supported Platforms:** Windows


#### Run it with `command_prompt`!  Elevation Required (e.g. root or admin) 

```
bcdedit.exe /set {default} bootstatuspolicy ignoreallfailures
bcdedit.exe /set {default} recoveryenabled no
```

<br/>
<br/>

## Atomic Test #4 - Windows - Overwrite file with Sysinternals SDelete
Overwrites and deletes a file using Sysinternals SDelete.
Requires the download of either Sysinternals Suite or the individual SDelete utility.

**Supported Platforms:** Windows


#### Inputs

| Name | Description | Type | Default Value | 
|:------:|:-------------:|:------:|:---------------:|
| file_to_overwrite | Path of file to overwrite and remove | Path | C:\some\file.txt|

#### Run it with `command_prompt`! 

```
sdelete.exe #{file_to_overwrite}
```

<br/>
<br/>
