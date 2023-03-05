# Xinit Virt Manager Guest
[heading__top]:
  #xinit-virt-manager-guest
  "&#x2B06; Start and attach to VM guest from TTY"


Start and attach to VM guest from TTY


## [![Byte size of Xinit Virt Manager Guest][badge__main__xinit_virt_manager_guest__source_code]][xinit_virt_manager_guest__main__source_code] [![Open Issues][badge__issues__xinit_virt_manager_guest]][issues__xinit_virt_manager_guest] [![Open Pull Requests][badge__pull_requests__xinit_virt_manager_guest]][pull_requests__xinit_virt_manager_guest] [![Latest commits][badge__commits__xinit_virt_manager_guest__main]][commits__xinit_virt_manager_guest__main]    [![License][badge__license]][branch__current__license]


---


- [:arrow_up: Top of Document][heading__top]

- [:building_construction: Requirements][heading__requirements]

- [:zap: Quick Start][heading__quick_start]

- [&#x1F9F0; Usage][heading__usage]

- [&#x1F5D2; Notes][heading__notes]

- [:chart_with_upwards_trend: Contributing][heading__contributing]

  - [:trident: Forking][heading__forking]
  - [:currency_exchange: Sponsor][heading__sponsor]

- [:card_index: Attribution][heading__attribution]

- [:balance_scale: Licensing][heading__license]


---



## Requirements
[heading__requirements]:
  #requirements
  "&#x1F3D7; Prerequisites and/or dependencies that this project needs to function properly"


> Prerequisites and/or dependencies that this project needs to function properly


This repository makes use of Git Submodules to track dependencies, to avoid
incomplete downloads clone with the `--recurse-submodules` option...


```Bash
git clone --recurse-submodules git@github.com:S0AndS0/xinit-virt-manager-guest.git
```


To update tracked Git Submodules issue the following commands...


```Bash
git pull

git submodule update --init --merge --recursive
```


To force upgrade of Git Submodules...


```Bash
git submodule update --init --merge --recursive --remote
```


> Note, forcing and update of Git Submodule tracked dependencies may cause
> instabilities and/or merge conflicts; if however everything operates as
> expected after an update please consider submitting a Pull Request.


______


## Quick Start
[heading__quick_start]:
  #quick-start
  "&#9889; Perhaps as easy as one, 2.0,..."


> Perhaps as easy as one, 2.0,...


- Download via `git`

```Bash
mkdir "${HOME}/git/hub/S0AndS0"
cd "${_}"

git clone --recurse-submodules git@github.com:S0AndS0/xinit-virt-manager-guest.git
```


- Generate installation configuration via `make`

```bash
cd "${HOME}/git/hub/S0AndS0/xinit-virt-manager-guest"

make config
```


- Edit `.config-make` file with preferred text editor

```bash
vim .config-make
```

> **Example configuration**
>
>     SCRIPT_NAME = xinit-virt-manager-guest
>     INSTALL_DIRECTORY = /home/s0ands0/.local/bin
>     __OS__ = Linux
>     __PATH_SEPARATOR__ = /
>     MAN_PATH = /home/s0ands0/.local/share/man
>     MAN_DIR_NAME = man1
>     GIT_BRANCH = main
>     GIT_REMOTE = origin
>     COMPLETION_DIR = /home/s0ands0/.local/share/bash-completion/completions
>
> Note; the `COMPLETION_DIR`, `INSTALL_DIRECTORY`, and `MAN_PATH` values may
> require adjustment if installing to a non-Arch (BTW™) derived distribution


- Install via `make`

```bash
make install
```


- Print available options via `--help` parameter

```bash
xinit-virt-manager-guest --help
```


______



## Usage
[heading__usage]:
  #usage
  "&#x1F9F0; How to utilize this repository"


> How to utilize this repository


- Switch to a TTY session without Xserver session

```bash
sudo chvt 2
```

> Note; many distributions allow for a keyboard shortcut to change active
> virtual terminal without escalating permissions, eg.
> <kbd>Alt</kbd>^<kbd>Ctrl</kbd>+<kbd>F2</kbd>


- Attach to graphical interface of virtual machine named `manjaro`

```bash
xinit-virt-manager-guest --display 2 --name manjaro
```

> Tip; to launch from another TTY consider levering the `openvt` command


______


## Notes
[heading__notes]:
  #notes
  "&#x1F5D2; Additional things to keep in mind when developing or utilizing this project"


> Additional things to keep in mind when developing or utilizing this project


This repository may not be feature complete and/or fully functional, Pull
Requests that add features or fix bugs are certainly welcomed.


Here are but a few known issues and _some_ workarounds;

- Window decorations cause lower portion of guest desktop to be inaccessible
> Reduce the resolution of guest... or win the battle with automating guest
> resolution updates

- Sound from host cuts-out
> Welcome back to the 90s :shrug: feel free to submit a Pull/Merge-Request

- Sound from guest does not work
> Welcome (again) to the 90s :shrug: feel free to submit a Pull/Merge-Request


______


## Contributing
[heading__contributing]:
  #contributing
  "&#x1F4C8; Options for contributing to xinit-virt-manager-guest and S0AndS0"


> Options for contributing to xinit-virt-manager-guest and S0AndS0


---


### Forking
[heading__forking]:
  #forking
  "&#x1F531; Tips for forking xinit-virt-manager-guest"


> Tips for forking xinit-virt-manager-guest


Start making a [Fork][xinit_virt_manager_guest__fork_it] of this repository to an account that you have write permissions for.


- Add remote for fork URL. The URL syntax is _`git@github.com:<NAME>/<REPO>.git`_...


```Bash
cd ~/git/hub/S0AndS0/xinit-virt-manager-guest

git remote add fork git@github.com:<NAME>/xinit-virt-manager-guest.git
```


- Commit your changes and push to your fork, eg. to fix an issue...


```Bash
cd ~/git/hub/S0AndS0/xinit-virt-manager-guest


git commit -F- <<'EOF'
:bug: Fixes #42 Issue


**Edits**


- `<SCRIPT-NAME>` script, fixes some bug reported in issue
EOF


git push fork main
```


> Note, the `-u` option may be used to set `fork` as the default remote, eg. _`git push -u fork main`_ however, this will also default the `fork` remote for pulling from too! Meaning that pulling updates from `origin` must be done explicitly, eg. _`git pull origin main`_


- Then on GitHub submit a Pull Request through the Web-UI, the URL syntax is _`https://github.com/<NAME>/<REPO>/pull/new/<BRANCH>`_


> Note; to decrease the chances of your Pull Request needing modifications before being accepted, please check the [dot-github](https://github.com/S0AndS0/.github) repository for detailed contributing guidelines.


---


### Sponsor
  [heading__sponsor]:
  #sponsor
  "&#x1F4B1; Methods for financially supporting S0AndS0 that maintains xinit-virt-manager-guest"


> Methods for financially supporting S0AndS0 that maintains xinit-virt-manager-guest


Thanks for even considering it!


Via Liberapay you may <sub>[![sponsor__shields_io__liberapay]][sponsor__link__liberapay]</sub> on a repeating basis.


Regardless of if you're able to financially support projects such as xinit-virt-manager-guest that S0AndS0 maintains, please consider sharing projects that are useful with others, because one of the goals of maintaining Open Source repositories is to provide value to the community.


______


## Attribution
[heading__attribution]:
  #attribution
  "&#x1F4C7; Resources that where helpful in building this project so far"


> Resources that where helpful in building this project so far


- [Arch Wiki -- `libvert`](https://wiki.archlinux.org/title/Libvirt)
- [GitHub -- `github-utilities/make-readme`](https://github.com/github-utilities/make-readme)
- [Kodi Forum -- How to run only Kodi without a desktop environment?](https://forum.kodi.tv/showthread.php?tid=324611)
- [Stack Overflow -- How to start GNOME Wayland session from command line/tty?](https://stackoverflow.com/questions/31213773/how-to-start-gnome-wayland-session-from-command-line-tty)
- [Super User -- How to stream audio through pipewire from one Linux system to another?](https://superuser.com/questions/1713253/how-to-stream-audio-through-pipewire-from-one-linux-system-to-another)
- [Unix Stack Exchange -- How to start a new GUI with custom command from tty1?](https://unix.stackexchange.com/questions/329374/how-to-start-a-new-gui-with-custom-command-from-tty1)
- [Unix Stack Exchange -- How to manually run/init/start a Xorg server on a different VT/TTY?](https://unix.stackexchange.com/questions/554592/how-to-manually-run-init-start-a-xorg-server-on-a-different-vt-tty)
- [Unix Stack Exchange -- How to open Virt-manager VM from command line?](https://unix.stackexchange.com/questions/704325/how-to-open-virt-manager-vm-from-command-line)


______


## License
[heading__license]:
  #license
  "&#x2696; Legal side of Open Source"


> Legal side of Open Source


```
Start and attach to VM guest from TTY
Copyright (C) 2023 S0AndS0

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, version 3 of the License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```


For further details review full length version of [AGPL-3.0][branch__current__license] License.



[branch__current__license]:
  /LICENSE
  "&#x2696; Full length version of AGPL-3.0 License"

[badge__license]:
  https://img.shields.io/github/license/S0AndS0/xinit-virt-manager-guest

[badge__commits__xinit_virt_manager_guest__main]:
  https://img.shields.io/github/last-commit/S0AndS0/xinit-virt-manager-guest/main.svg

[commits__xinit_virt_manager_guest__main]:
  https://github.com/S0AndS0/xinit-virt-manager-guest/commits/main
  "&#x1F4DD; History of changes on this branch"


[xinit_virt_manager_guest__community]:
  https://github.com/S0AndS0/xinit-virt-manager-guest/community
  "&#x1F331; Dedicated to functioning code"


[issues__xinit_virt_manager_guest]:
  https://github.com/S0AndS0/xinit-virt-manager-guest/issues
  "&#x2622; Search for and _bump_ existing issues or open new issues for project maintainer to address."

[xinit_virt_manager_guest__fork_it]:
  https://github.com/S0AndS0/xinit-virt-manager-guest/fork
  "&#x1F531; Fork it!"

[pull_requests__xinit_virt_manager_guest]:
  https://github.com/S0AndS0/xinit-virt-manager-guest/pulls
  "&#x1F3D7; Pull Request friendly, though please check the Community guidelines"

[xinit_virt_manager_guest__main__source_code]:
  https://github.com/S0AndS0/xinit-virt-manager-guest/
  "&#x2328; Project source!"

[badge__issues__xinit_virt_manager_guest]:
  https://img.shields.io/github/issues/S0AndS0/xinit-virt-manager-guest.svg

[badge__pull_requests__xinit_virt_manager_guest]:
  https://img.shields.io/github/issues-pr/S0AndS0/xinit-virt-manager-guest.svg

[badge__main__xinit_virt_manager_guest__source_code]:
  https://img.shields.io/github/repo-size/S0AndS0/xinit-virt-manager-guest


[sponsor__shields_io__liberapay]:
  https://img.shields.io/static/v1?logo=liberapay&label=Sponsor&message=S0AndS0

[sponsor__link__liberapay]:
  https://liberapay.com/S0AndS0
  "&#x1F4B1; Sponsor developments and projects that S0AndS0 maintains via Liberapay"

