---
published: true
title: T1002 - Data Compressed
---
## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1002)
<blockquote>An adversary may compress data (e.g., sensitive documents) that is collected prior to exfiltration in order to make it portable and minimize the amount of data sent over the network. The compression is done separately from the exfiltration channel and is performed using a custom program or algorithm, or a more common compression library or utility such as 7zip, RAR, ZIP, or zlib.</blockquote>

## Atomic Tests

- [Atomic Test #1 - Compress Data for Exfiltration With PowerShell]

- [Atomic Test #2 - Compress Data for Exfiltration With Rar]

<br/>

## Atomic Test #1 - Compress Data for Exfiltration With PowerShell
An adversary may compress data (e.g., sensitive documents) that is collected prior to exfiltration 

**Supported Platforms:** Windows


#### Inputs

| Name | Description | Type | Default Value | 
|:------:|:-------------:|:------:|:---------------:|
| input_file | Path that should be compressed into our output file | Path | C:\*|
| output_file | Path where resulting compressed data should be placed | Path | C:\test\Data.zip|

#### Run it with `powershell`!

```
dir #{input_file} -Recurse | Compress-Archive -DestinationPath #{output_file}
```
<br/>
<br/>

## Atomic Test #2 - Compress Data for Exfiltration With Rar
An adversary may compress data (e.g., sensitive documents) that is collected prior to exfiltration 

**Supported Platforms:** Windows


#### Inputs

| Name | Description | Type | Default Value | 
|:------:|:-------------:|:------:|:---------------:|
| input_file | Path that should be compressed into our output file | Path | *.docx|
| output_file | Path where resulting compressed data should be placed | Path | exfilthis.rar|

#### Run it with `command_prompt`!

```
rar a -r #{output_file} #{input_file}
```
<br/>
<br/>