# MITRE ATT&CK

## Windows Atomic Tests by ATT&CK Tactic & Technique

### defense evasion

- [T1134 Access Token Manipulation](_posts/2019-06-20-T1134 - Access-Token-Manipulation.md)
	- Atomic Test #1: Access Token Manipulation [windows]
- [T1197 BITS Jobs](_posts/2019-06-25-T1197 - BITS Jobs.md)
	- Atomic Test #1: Download & Execute [windows]
	- Atomic Test #2: Download & Execute via PowerShell BITS [windows]
	- Atomic Test #3: Persist, Download, & Execute [windows]

### privilege-escalation

- [T1134 Access Token Manipulation](_posts/2019-06-20-T1134 - Access-Token-Manipulation.md)
	- Atomic Test #1: Access Token Manipulation [windows]
- [T1015 Accessibility Features](_posts/2019-06-27-T1015 - Accessibility Features.md)
  - Atomic Test #1: Attaches Command Prompt As Debugger To Process - osk [windows]
  - Atomic Test #2: Attaches Command Prompt As Debugger To Process - sethc [windows]
  - Atomic Test #3: Attaches Command Prompt As Debugger To Process - utilman [windows]
  - Atomic Test #4: Attaches Command Prompt As Debugger To Process - magnify [windows]
  - Atomic Test #5: Attaches Command Prompt As Debugger To Process - narrator [windows]
  - Atomic Test #6: Attaches Command Prompt As Debugger To Process - DisplaySwitch [windows]
  - Atomic Test #7: Attaches Command Prompt As Debugger To Process - AtBroker [windows]
  
### persistence

- [T1015 Accessibility Features](_posts/2019-06-27-T1015 - Accessibility Features.md)
  - Atomic Test #1: Attaches Command Prompt As Debugger To Process - osk [windows]
  - Atomic Test #2: Attaches Command Prompt As Debugger To Process - sethc [windows]
  - Atomic Test #3: Attaches Command Prompt As Debugger To Process - utilman [windows]
  - Atomic Test #4: Attaches Command Prompt As Debugger To Process - magnify [windows]
  - Atomic Test #5: Attaches Command Prompt As Debugger To Process - narrator [windows]
  - Atomic Test #6: Attaches Command Prompt As Debugger To Process - DisplaySwitch [windows]
  - Atomic Test #7: Attaches Command Prompt As Debugger To Process - AtBroker [windows]  
- [T1098 Account Manipulation](_posts/2019-06-27-T1098 - Account Manipulation.md)
  - Atomic Test #1: Admin Account Manipulate [windows]

### discovery

- [T1087 Account Discovery](_posts/2019-06-28-T1087 - Account Discovery.md)
  - Atomic Test #8: Enumerate all accounts [windows]
  - Atomic Test #9: Enumerate all accounts via PowerShell [windows]
  - Atomic Test #10: Enumerate logged on users [windows]
  - Atomic Test #11: Enumerate logged on users via PowerShell [windows]
- [T1010 Application Window Discovery](_posts/2019-07-01-T1010 - Application Window Discovery.md)
  - Atomic Test #1: List Process Main Windows - C# .NET [windows]

### credential-access

- [T1098 Account Manipulation](_posts/2019-06-27-T1098 - Account Manipulation.md)
  - Atomic Test #1: Admin Account Manipulate [windows]
- [T1110 Brute Force](_posts/2019-07-10-T1110 Brute Force.md)
  - Atomic Test #1: Brute Force Credentials [windows]
- T1003 Credential Dumping
  - Atomic Test #1: Powershell Mimikatz [windows]
  - Atomic Test #2: Gsecdump [windows]
  - Atomic Test #3: Windows Credential Editor [windows]
  - Atomic Test #4: Registry dump of SAM, creds, and secrets [windows]
  - Atomic Test #5: Dump LSASS.exe Memory using ProcDump [windows]
  - Atomic Test #6: Dump LSASS.exe Memory using Windows Task Manager [windows]
  - Atomic Test #7: Offline Credential Theft With Mimikatz [windows]
  - Atomic Test #8: Dump Active Directory Database with NTDSUtil [windows]
  - Atomic Test #9: Create Volume Shadow Copy with NTDS.dit [windows]
  - Atomic Test #10: Copy NTDS.dit from Volume Shadow Copy [windows]
- T1081 Credentials in Files
  - Atomic Test #3: Mimikatz & Kittenz [windows]
  - Atomic Test #4: Extracting credentials from files [windows]
- T1214 Credentials in Registry
  - Atomic Test #1: Enumeration for Credentials in Registry [windows]
- T1179 Hooking
  - Atomic Test #1: Hook PowerShell TLS Encrypt/Decrypt Messages [windows]
- T1056 Input Capture
  - Atomic Test #1: Input Capture [windows]
- T1141 Input Prompt
  - Atomic Test #2: PowerShell - Prompt User for Password [windows]
- T1040 Network Sniffing
  - Atomic Test #3: Packet Capture Windows Command Prompt [windows]
  - Atomic Test #4: Packet Capture PowerShell [windows]
- T1174 Password Filter DLL
  - Atomic Test #1: Install and Register Password Filter DLL [windows]
- T1145 Private Keys
  - Atomic Test #1: Private Keys [windows]
  
### lateral-movement

- [T1037 Logon Scripts](_posts/2019-07-10-T1037 Logon Scripts.md)
  - Atomic Test #1: Logon Scripts [windows]
- [T1075 Pass the Hash](_posts/2019-07-10-T1075 - Pass the Hash.md)
  - Atomic Test #1: Mimikatz Pass the Hash [windows]
  - Atomic Test #2: Mimikatz Kerberos Ticket Attack [windows]
  
### collection

- [T1123 Audio Capture](_posts/2019-07-10-T1123 Audio Capture.md) 
  - Atomic Test #1: SourceRecorder via Windows command prompt [windows]
  - Atomic Test #2: PowerShell Cmdlet via Windows command prompt [windows]
- [T1119 Automated Collection](_posts/2019-07-10-T1119 - Automated Collection.md)
  - Atomic Test #1: Automated Collection Command Prompt [windows]
  - Atomic Test #2: Automated Collection PowerShell [windows]
  
### exfiltration

- [T1002 Data Compressed](_posts/2019-08-27-T1002 - Data Compressed.md)
  - Atomic Test #1: Compress Data for Exfiltration With PowerShell [windows]
  - Atomic Test #2: Compress Data for Exfiltration With Rar [windows]
  
- T1022 Data Encrypted
  - Atomic Test #1: Compress Data and lock with password for Exfiltration with winrar [windows]
  - Atomic Test #2: Compress Data and lock with password for Exfiltration with winzip [windows]
  - Atomic Test #3: Compress Data and lock with password for Exfiltration with 7zip [windows]


