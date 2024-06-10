# PowerShell-7.4-LTS
Installation on Debian 11 or 12 via the Package Repository - Debian uses APT (Advanced Package Tool) as a package manager.

This commands only works for supported versions of Debian.

-------------------------------------------------------------------------------------------------------------------

#### Prerequisites

#### Update the list of packages
$ sudo apt-get update

#### Install pre-requisite packages.
$ sudo apt-get install -y wget

#### Get the version of Debian
$ source /etc/os-release

#### Download the Microsoft repository GPG keys
$ wget -q https://packages.microsoft.com/config/debian/$VERSION_ID/packages-microsoft-prod.deb

#### Register the Microsoft repository GPG keys
$ sudo dpkg -i packages-microsoft-prod.deb

#### Delete the Microsoft repository GPG keys file
$ rm packages-microsoft-prod.deb

#### Update the list of packages after we added packages.microsoft.com
$ sudo apt-get update

#### Install PowerShell
$ sudo apt-get install -y powershell

#### Start PowerShell
$ pwsh

-------------------------------------------------------------------------------------------------------------------

Installation via direct download.

#### Prerequisites

#### Update the list of packages
$ sudo apt-get update

#### Install pre-requisite packages.
$ sudo apt-get install -y wget

#### Download the PowerShell package file
$ wget https://github.com/PowerShell/PowerShell/releases/download/v7.4.2/powershell_7.4.2-1.deb_amd64.deb

#### Install the PowerShell package
$ sudo dpkg -i powershell_7.4.2-1.deb_amd64.deb

#### Resolve missing dependencies and finish the install (if necessary)
$ sudo apt-get install -f

#### Delete the downloaded package file
$ rm powershell_7.4.2-1.deb_amd64.deb

#### Start PowerShell
$ pwsh

-------------------------------------------------------------------------------------------------------------------

Uninstall PowerShell

$ sudo apt-get remove powershell

-------------------------------------------------------------------------------------------------------------------

NOTE: Debian 11 (Bullseye) - OS support ends on 31-jul-2024. Debian 12 (Bookworm) - OS support ends on 10-jun-2026.

Author
<br>
Ravi Shankar Tekkam (projects Head)
