# `Wake-on-LAN.ps1`: a [Wake-on-LAN](https://en.wikipedia.org/wiki/Wake-on-LAN) PowerShell script

## `Wake-on-LAN.ps1` PowerShell script for sending Wake-on-LAN magic packets to given machine's hardware MAC address

This script originated is a modification [[Wayback]](https://web.archive.org/web/20210909182144/https://docs.microsoft.com/en-gb/archive/blogs/matthts/wakeup-machines-a-powershell-script-for-wake-on-lan) [`WakeUp-Machines.ps1`](https://docs.microsoft.com/en-gb/archive/blogs/matthts/wakeup-machines-a-powershell-script-for-wake-on-lan) by [Matthijs ten Seldam](https://nl.linkedin.com/in/matthts), Microsoft that has the drawback of requiring a text file with the machines to wake up, and (before his change) the original reliance on the above mentioned [[Wayback]](https://web.archive.org/web/20210914123109/https://www.depicus.com/wake-on-lan/wake-on-lan-cmd) [`WolCmd.exe`](https://www.depicus.com/wake-on-lan/wake-on-lan-cmd) in the current directory.

[[Wayback]](https://web.archive.org/web/20210918182919/https://gist.github.com/alimbada) [Ammaar Limbada](https://gist.github.com/alimbada) modified it to take a hardware [MAC address](https://en.wikipedia.org/wiki/MAC_address#Notational_conventions) on the command-line, but unlike the [[Wayback]](https://web.archive.org/web/20210620134205/https://github.com/jpoliv/wakeonlan/blob/master/wakeonlan) [Perl `wakeonlan` script](https://web.archive.org/web/20210620134205/https://github.com/jpoliv/wakeonlan/blob/master/wakeonlan) that is available for most Linux and BSD systems, it was limited to Windows and pure hex (Intel Landesk) formatted hardware MAC Addresses.

`wakeonlan` supports these formats or ["notational conventions"](https://en.wikipedia.org/wiki/MAC_address#Notational_conventions):

- `xx:xx:xx:xx:xx:xx` (canonical)
- `xx-xx-xx-xx-xx-xx` (Windows)
- `xxxxxx-xxxxxx` (Hewlett-Packard switches)
- `xxxxxxxxxxxx` (Intel Landesk)

Goal is to have this script support all of them too (:
