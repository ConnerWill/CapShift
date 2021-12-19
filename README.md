![CAPshift Banner](media/CAPshift-Banner.png)

# CAPshift
[**CAPshift.ahk**](https://github.com/ConnerWill/CAPshift) extends the functionality of the the **CapsLock** key.
It allows you to disable unused/annoying keys along with providing formatting of  selected text and text replacement.

* [CAPshift](#capshift)
* [Overview](#overview)
* [Hotkeys](#hotkeys)
* [Key States](#key-states)
   * [Caps Lock](#caps-lock)
   * [NumLock](#numlock)
   * [Scroll Lock](#scroll-lock)
* [Usage](#usage)
* [Configuration File](#configuration-file)
   * [ini Values Descriptions](#ini-values-descriptions)
   * [Configuration File Contents](#configuration-file-contents)
   * [Customizing Hotkeys](#customizing-hotkeys)
* [Running on boot](#running-on-boot)
   * [Standard - <em>(Small-Brain method)</em>](#standard---small-brain-method)
   * [Smart - <em>(Big-Brain Method)</em>](#smart---big-brain-method)
   * [Permanent Method - <em>(Task Scheduler (Chad) Method)</em>](#permanent-method---task-scheduler-chad-method)
* [Other](#other)

# Overview
This script allows you to set the desired key state of keys on your keyboard; while still allowing you to use those keys without changing settings or killing the script. It also adds a popup menu that can format the currently selected text.

# Hotkeys

Action | Keys | Press Key Time (Seconds)
--- | :-: | :-:
*Holding* <kbd>`CapsLock`</kbd> for `0.5` seconds *(or user defined time)* toggles CapsLock **ON** or **OFF**|<kbd>`CapsLock`</kbd>|`0.5`
**Holding** <kbd>`CapsLock`</kbd>** for `1` second *(or user defined time)*  displays a popup tooltip menu.|<kbd>`CapsLock`</kbd>|`1`
**Holding** <kbd>`F1`</kbd> for `0.5` seconds *(or user defined time)* presses <kbd>`F1`</kbd> once.|<kbd>`F1`</kbd>|`0.5`
**Holding** <kbd>`NumLock`</kbd> for `0.5` seconds *(or user defined time)*, Toggles number pad locking. *(Default **Number Lock** state is **Enabled**)*|<kbd>`NumLock`</kbd> |`0.5`
**Holding** <kbd>`ScrollLock`</kbd> for `0.5` seconds *(or user defined time)* toggles CapsLock **ON** or **OFF**|<kbd>`ScrollLock`</kbd>|`0.5`

*You can also customize the hotkeys and actions as described in the **"Customizing Hotkeys"** section below.*

# Key States

## Caps Lock
Sometimes abbreviated as <kbd>`CAPS`</kbd> or <kbd>`CAPSLK`</kbd>, Caps Lock is a toggle key on a computer keyboard, that when pressed, causes all letters typed to be in uppercase. It allows you to switch the letters on your keyboard from lowercase to uppercase. If you press the Caps Lock key to enable Caps Lock, every letter you type on the keyboard will be automatically capitalized until you press it again to disable it. For example, when Caps Lock is enabled, the typed letters appear "**LIKE THIS**". When disabled, they appear "**like this**".

## NumLock
Short for numeric lock or number lock, the Num key, Num Lock, or Num Lk key is on the top-left corner of a keyboard's numeric keypad. The Num Lock key enables and disables the numeric pad.

When *'Num Lock'* is enabled, you can use the numbers on the keypad. When *'Num Lock'* is disabled, pressing those keys activates those key's alternate function. For instance, the arrow keys on the keypad may only be used if *'Num Lock'* is disabled.

**Num lock keys:**

Below is a chart with additional information about what each numeric keypad key does when *'Num Lock'* is enabled and disabled. For example, pressing the <kbd>`2`</kbd> key on the numeric keypad when *'Num Lock'* is enabled enters the number <kbd>`2`</kbd>, and when *'Num Lock'* is off, it will arrow down one line.

Key|Num lock enabled|Num lock disabled
--- | :-: | :-:
<kbd>`0`</kbd>|0|Ins
<kbd>`1`</kbd>|1|End
<kbd>`2`</kbd>|2|Down arrow
<kbd>`3`</kbd>|3|PgDn
<kbd>`4`</kbd>|4|Left arrow
<kbd>`5`</kbd>|5|Nothing
<kbd>`6`</kbd>|6|Right arrow
<kbd>`7`</kbd>|7|Home
<kbd>`8`</kbd>|8|Up arrow
<kbd>`9`</kbd>|9|PgUp
<kbd>`.`</kbd>|.|Del

## Scroll Lock
Sometimes abbreviated as <kbd>`ScLk`</kbd>, <kbd>`ScrLk`</kbd>, or <kbd>`Slk`</kbd>, the *'Scroll Lock'* key is found on a computer keyboard, often located close to the pause key. The Scroll Lock key was initially intended to be used in conjunction with the arrow keys to scroll through the contents of a text box. It has also been used to stop the scrolling of text or halt the operation of a program. Today, the key is not often used.

# Usage
[Install AutoHotkey](https://autohotkey.com/download/), then run the [`CAPshift.ahk`](https://github.com/ConnerWill/CAPshift/blob/main/CAPshift.ahk) script (open with AutoHotkey if prompted).

# Configuration File

## Customizing Hotkeys
To change the settings/behavior of this script, modify the [`CAPshift.ini`](https://github.com/ConnerWill/CAPshift/blob/main/CAPshift.ini) script and then run the [`CAPshift.ahk`](https://github.com/ConnerWill/CAPshift/blob/main/CAPshift.ahk) *(program will restart if it's already running).*

**Note:*
>>`!` *corresponds to* <kbd>`Alt`</kbd>
>
>>`+` *corresponds to*  <kbd>`Shift`</kbd>
>
>>`#` *corresponds to*  <kbd>`Win`</kbd>
>
>>`^` *corresponds to*  <kbd>`Ctrl`</kbd>

*A more detailed description of hotkeys can be found here: [AutoHotkey docs](https://autohotkey.com/docs/Hotkeys.htm).*<br>

*After any changes to the [`CAPshift.ini`](https://github.com/ConnerWill/CAPshift/blob/main/CAPshift.ini) configuration file, the program needs to be closed and opened again.*

## Configuration File Contents

[`CAPshift.ini`](https://github.com/ConnerWill/CAPshift/blob/main/CAPshift.ini) contents
```
;\[Settings]
;capslockidle=120    ;0-999  0=Off  Seconds to wait before turning off CapsLock when the keyboard is idle
;showstatus=1        ;0,1    0=Hide  1=Show  Hide or show the status windows
;delaycapslock=1     ;0,1    0=Ignore CapsLock  1=Delay F1
;delayf1=1           ;0,1    0=Ignore F1  1=Delay F1
;delayinsert=1
;delayscrolllock=1
;delaynumlock=1
;
;ae=æ                ;Chars to replace=Chars to replace with
;oe=ø                ;Special characters:
;aa=å                ;  .space. .tab. .return. .newline. .comma. .semicolon.
;AE=Æ
;OE=Ø
;AA=Å
;AA=Å
;.return..newline..return..newline.=

\[Settings]
capslockidle=120
showstatus=1
delaycapslock=1
delayf1=1
delayinsert=1
delayscrolllock=1
delaynumlock=1

ae=æ
oe=ø
aa=å
AE=Æ
OE=Ø
AA=Å
```

## ini Values Descriptions
Variable|Value|Description
--- | :--: | :-:
```capslockidle```|Range: `0-999` `0`=Off|```Seconds``` to wait before **turning off** <kbd>`CapsLock`</kbd> when the keyboard is idle.
```showstatus```|`0`=Hide `1`=Show|```Hide``` *or* ```show``` the status windows.
```delaycapslock```|`0`=Ignore `1`=Delay|```Enable``` *Or* ```Disable``` the script from affecting <kbd>`CapsLock`</kbd>.
```delayf1```|`0`=Ignore  `1`=Delay |```Enable``` *Or* ```Disable``` the script from affecting <kbd>`F1`</kbd>.
```delayinsert```|`0`=Ignore `1`=Delay|```Enable``` *Or* ```Disable``` the script from affecting <kbd>`Insert`</kbd>.
```delayscrolllock```|`0`=Ignore <kbd>`F1`</kbd> `1`=Delay ScrollLock|```Enable``` *Or* ```Disable``` the script from affecting <kbd>`ScrollLock`</kbd>.
```delaynumlock```|`0`=Ignore <kbd>`F1`</kbd> `1`=Delay|```Enable``` *Or* ```Disable``` the script from affecting <kbd>`NumLock`</kbd>.

Character Replacement

```ae=æ```,```oe=ø```,```aa=å```,```AE=Æ```,```OE=Ø```,```AA=Å```,```AA=Å```

``.return..newline..return..newline.=.space..tab..return..newline..comma..semicolon.``
```
*e.g.*
```ggg=GeeGeeGee```
: *'ggg'* will be replaced with *'GeeGeeGee'*
```

# Running on boot

You can make the script run on every boot with either of these methods.

## **Standard** - *`(Small-Brain method)`*

1. Press <kbd>`Win`</kbd> + <kbd>`R`</kbd>, enter `shell:startup`, then click <kbd>OK</kbd>
2. Create a shortcut to the [`CAPshift.ahk`](https://github.com/ConnerWill/CAPshift/blob/main/CAPshift.ahk) in your startup folder.

## **Smart** - *`(Big-Brain Method)`*

Since the function of this script is to add scripts to the startup folder, you can just use this script to add itself to the startup folder.

You can do this by running the [`AutoStartupToggle.ahk`](https://github.com/ConnerWill) file (*Coming Soon ...*).

Then select the [`CAPshift.ahk`](https://github.com/ConnerWill/CAPshift/blob/main/CAPshift.ahk) file and press the **Hotkey** to add the selected file to the startup folder.

You can confirm the script has been added to the startup folder by pressing the **Hotkey** to display the **Startup Folder** shortcuts.

## **Permanent Method** - *`(Task Scheduler (Chad) Method)`*
**Run the following commands in an Administrator powershell prompt.**

*Be sure to specify the correct path to your CAPshift.ahk file.*
```
$A = "PATH\TO\CAPshift.ahk"

$T = New-ScheduledTaskAction -Execute "PATH\TO\CAPshift.ahk"

$P = New-ScheduledTaskTrigger -AtLogon

$S = New-ScheduledTaskPrincipal -GroupId "BUILTIN\Administrators" -RunLevel Highest

$F = New-ScheduledTaskSettingsSet -AllowStartIfOnBatteries -DontStopIfGoingOnBatteries -ExecutionTimeLimit 0

$D = New-ScheduledTask -Action $A -Principal $P -Trigger $T -Settings $S

Register-ScheduledTask CAPshift -InputObject $D
```

The task is now registered and will run on the next logon, and can be viewed or modified in *'Task Scheduler'*.

---

## Other
*To see debug messages, download [SysInternals DebugView](https://technet.microsoft.com/en-us/sysinternals/debugview).*

*Credit to [original script](https://www.autohotkey.com/boards/viewtopic.php?t=69889)*
