---
title: T1010 - Application Window Discovery
published: true
---
## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1010)
<blockquote>Adversaries may attempt to get a listing of open application windows. Window listings could convey information about how the system is used or give context to information collected by a keylogger.

In Mac, this can be done natively with a small <a href="https://attack.mitre.org/techniques/T1155">AppleScript</a> script.</blockquote>

## Atomic Tests
<br/>
- Atomic Test #1 - List Process Main Windows - C# .NET

<br/>

## Atomic Test #1 - List Process Main Windows - C# .NET
Compiles and executes C# code to list main window titles associated with each process.

**Supported Platforms:** Windows

#### Inputs

| Name | Description | Type | Default Value | 
|:------:|:-------------:|:------:|:---------------:|
| input_source_code | Path to source of C# code | path | <a href="https://github.com/achakrabortty/Bitdefender-EPP-Playbook/blob/gh-pages/_posts/codes/T1010/T1010.cs">File</a> |
| output_file_name | Name of output binary | string | T1010.exe|

#### Run it with `command_prompt`!

```
C:\Windows\Microsoft.NET\Framework\v4.0.30319\csc.exe -out:#{output_file_name} #{input_source_code}
#{output_file_name}
```
<br/>
