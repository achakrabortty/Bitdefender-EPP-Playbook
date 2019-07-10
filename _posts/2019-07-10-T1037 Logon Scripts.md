---
published: false
---
## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1037)
<blockquote>
<b>Windows</b>
Windows allows logon scripts to be run whenever a specific user or group of users log into a system. (Citation: TechNet Logon Scripts) The scripts can be used to perform administrative functions, which may often execute other programs or send information to an internal logging server.
<br/>
<br/> 
If adversaries can access these scripts, they may insert additional code into the logon script to execute their tools when a user logs in. This code can allow them to maintain persistence on a single system, if it is a local script, or to move laterally within a network, if the script is stored on a central server and pushed to many systems. Depending on the access configuration of the logon scripts, either local credentials or an administrator account may be necessary.
<br/>
<br/>  
<b>Mac</b>
Mac allows login and logoff hooks to be run as root whenever a specific user logs into or out of a system. A login hook tells Mac OS X to execute a certain script when a user logs in, but unlike startup items, a login hook executes as root (Citation: creating login hook). There can only be one login hook at a time though. If adversaries can access these scripts, they can insert additional code to the script to execute their tools when a user logs in.</blockquote>

## Atomic Tests

- Atomic Test #1 - Logon Scripts

- Atomic Test #2 - Logon Scripts - Mac

<br/>

## Atomic Test #1 - Logon Scripts
Added Via Reg.exe

**Supported Platforms:** Windows


#### Inputs

| Name | Description | Type | Default Value | 
|:------:|:-------------:|:------:|:---------------:|
| script_command | Command To Execute | String | cmd.exe /c calc.exe|

#### Run it with `command_prompt`!

```
REG.exe ADD HKCU\Environment /v UserInitMprLogonScript /t REG_MULTI_SZ /d "#{script_command}"
```
<br/>
<br/>

## Atomic Test #2 - Logon Scripts - Mac
Mac logon script

**Supported Platforms:** macOS

#### Run it with these steps!

1. Create the required plist file

    <code>sudo touch /private/var/root/Library/Preferences/com.apple.loginwindow.plist</code>

2. Populate the plist with the location of your shell script

    <code>sudo defaults write com.apple.loginwindow LoginHook /Library/Scripts/AtomicRedTeam.sh</code>

3. Create the required plist file in the target user's Preferences directory

	  <code>touch /Users/$USER/Library/Preferences/com.apple.loginwindow.plist</code>

4. Populate the plist with the location of your shell script

	  <code>defaults write com.apple.loginwindow LoginHook /Library/Scripts/AtomicRedTeam.sh</code>

