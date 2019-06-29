---
published: true
title: T1087 - Account Discovery
---

## [Description from ATT&CK](https://attack.mitre.org/wiki/Technique/T1087)
<blockquote>Adversaries may attempt to get a listing of local system or domain accounts. 

<b>Windows</b>
Example commands that can acquire this information are <code>net user</code>, <code>net group <groupname></code>, and <code>net localgroup <groupname></code> using the <a href="https://attack.mitre.org/software/S0039">Net</a> utility or through use of <a href="https://attack.mitre.org/software/S0105">dsquery</a>. If adversaries attempt to identify the primary user, currently logged in user, or set of users that commonly uses a system, <a href="https://attack.mitre.org/techniques/T1033">System Owner/User Discovery</a> may apply.
<br /><br />

<b>Mac</b>
On Mac, groups can be enumerated through the <code>groups</code> and <code>id</code> commands. In mac specifically, <code>dscl . list /Groups</code> and <code>dscacheutil -q group</code> can also be used to enumerate groups and users.
<br /><br />

<b>Linux</b>
On Linux, local users can be enumerated through the use of the <code>/etc/passwd</code> file which is world readable. In mac, this same file is only used in single-user mode in addition to the <code>/etc/master.passwd</code> file.
<br /><br />

Also, groups can be enumerated through the <code>groups</code> and <code>id</code> commands</blockquote>
