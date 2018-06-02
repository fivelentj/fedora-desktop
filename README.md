# fedora-desktop

Created to take the 'Minimal Install' version of Fedora and install my desktop setup on it.

### Prerequisites

Requires Ansible be installed on the machine to run the Ansible playbooks.

### Installing

Download a copy of the project to your machine:

```
git clone git@github.com:fivelentj/fedora-desktop.git ~/fedora-desktop
```

Navigate to the created directory and run the ansible playbook:
```
cd ~/fedora-desktop
ansible-playbook config_desktop.yaml -K
```
(Required -K to run certain tasks under sudo)

### Modules and packages  installed
Can comment out any module from the config_desktop.yaml file to skip installation.

Common:
 - vim-enhanced: Some installs come with vim-minimal. This will swap that out.
  - rxvt-unicode: lightweight terminal emulator.
  - feh: used to set wallpapers.
  - vundle: a package manager for Vim.
  - ImageMagick: Image processor
  - Neovim: vim replacement
  - pywal: Used to set color themes to various applicatinos
  
i3gaps: Builds the latest [i3-gaps](https://github.com/Airblader/i3) from source.

compton: Used for transparancy in i3 and stops my virtual box instances from tearing.

lightdm: Installs lightdm and slick-greeter for a better looking login screen.

polybar: Builds the latest [polybar](https://github.com/jaagr/polybar) from source. Used as a replacement for the default status bar.

rofi: Builds the latest [rofi](https://github.com/DaveDavenport/rofi) from source. Used a replacement for dmenu.

virtualbox: Installs the pre-req packages to install the guest additions for VirtualBox. Will still need to run the install script manually.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
