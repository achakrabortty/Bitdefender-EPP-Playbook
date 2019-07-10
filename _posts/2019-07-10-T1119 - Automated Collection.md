---
title: T1119 - Automated Collection
published: true
---
## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1119)
<blockquote>Once established within a system or network, an adversary may use automated techniques for collecting internal data. Methods for performing this technique could include use of <a href="https://attack.mitre.org/techniques/T1064">Scripting</a> to search for and copy information fitting set criteria such as file type, location, or name at specific time intervals. This functionality could also be built into remote access tools. <br/>
<br/>
This technique may incorporate use of other techniques such as <a href="https://attack.mitre.org/techniques/T1083">File and Directory Discovery</a> and <a href="https://attack.mitre.org/techniques/T1105">Remote File Copy</a> to identify and move files.</blockquote>

## Atomic Tests

- Atomic Test #1 - Automated Collection Command Prompt

- Atomic Test #2 - Automated Collection PowerShell

<br/>

## Atomic Test #1 - Automated Collection Command Prompt
Automated Collection

**Supported Platforms:** Windows

#### Run it with `command_prompt`!

```
dir c: /b /s .docx | findstr /e .docx
for /R c: %f in (*.docx) do copy %f c:\temp\
```
<br/>
<br/>

## Atomic Test #2 - Automated Collection PowerShell
Automated Collection

**Supported Platforms:** Windows

#### Run it with `powershell`!

```
Get-ChildItem -Recurse -Include *.doc | % {Copy-Item $_.FullName -destination c:\temp}
```
