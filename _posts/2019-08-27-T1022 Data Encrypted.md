---
published: true
title: T1022 Data Encrypted
---
## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1022)
<blockquote>Data is encrypted before being exfiltrated in order to hide the information that is being exfiltrated from detection or to make the exfiltration less conspicuous upon inspection by a defender. The encryption is performed by a utility, programming library, or custom algorithm on the data itself and is considered separate from any encryption performed by the command and control or file transfer protocol. Common file archive formats that can encrypt files are RAR and zip.

Other exfiltration techniques likely apply as well to transfer the information out of the network, such as < a href="https://attack.mitre.org/techniques/T1041">Exfiltration Over Command and Control Channel</a> and <a href="https://attack.mitre.org/techniques/T1048">Exfiltration Over Alternative Protocol</a></blockquote>

## Atomic Tests

- [Atomic Test #1 - Compress Data and lock with password for Exfiltration with winrar]

- [Atomic Test #2 - Compress Data and lock with password for Exfiltration with winzip]

- [Atomic Test #3 - Compress Data and lock with password for Exfiltration with 7zip]


<br/>

## Atomic Test #1 - Compress Data and lock with password for Exfiltration with winrar
Note: Requires winrar installation
rar a -p"blue" hello.rar (VARIANT)

**Supported Platforms:** Windows


#### Run it with `command_prompt`!

```
mkdir ./tmp/victim-files
cd ./tmp/victim-files
echo "This file will be encrypted" > ./encrypted_file.txt
rar a -hp"blue" hello.rar
dir
```

<br/>
<br/>

## Atomic Test #2 - Compress Data and lock with password for Exfiltration with winzip
Note: Requires winzip installation
wzzip sample.zip -s"blueblue" *.txt (VARIANT)

**Supported Platforms:** Windows


#### Run it with `command_prompt`!

```
path=%path%;"C:\Program Files (x86)\winzip"
mkdir ./tmp/victim-files
cd ./tmp/victim-files
echo "This file will be encrypted" > ./encrypted_file.txt
winzip32 -min -a -s"hello" archive.zip *
dir
```

<br/>
<br/>

## Atomic Test #3 - Compress Data and lock with password for Exfiltration with 7zip
Note: Requires 7zip installation

**Supported Platforms:** Windows


#### Run it with `command_prompt`!

```
mkdir ./tmp/victim-files
cd ./tmp/victim-files
echo "This file will be encrypted" > ./encrypted_file.txt
7z a archive.7z -pblue
dir
```

<br/>
