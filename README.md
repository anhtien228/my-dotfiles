# Tien's dotfiles
Storing all configurations for prompt engines that I have been used.
Inspired from [devaslife's setup](https://github.com/craftzdog/dotfiles)

# Contents
- PowerShell config
- git config
- putty config (SSH)

## PowerShell setup (Windows)
- Windows 11 (Recommened for customized theme)
- [Powershell 7](https://github.com/PowerShell/PowerShell/releases) (Recommended)
- [Git for Windows](https://git-scm.com/download/win)
- [Oh My Posh](https://ohmyposh.dev/) - Prompt engine theme
- [Terminal Icons](https://github.com/devblackops/Terminal-Icons) - Folder and file icons
- [PSReadLine](https://docs.microsoft.com/en-us/powershell/module/psreadline/) - Module for customize editing env, autocompletion, history
- [z](https://www.powershellgallery.com/packages/z/1.1.13) or [zoxide](https://github.com/ajeetdsouza/zoxide) - Directory jumper
- [PSFzf](https://github.com/kelleyma49/PSFzf) - Fuzzy finder

## Universal fonts and theme
- Font: [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) - Fira Code NFM
- Themes: [Catppuccin Macchiato](https://github.com/catppuccin/catppuccin)

## How to use
- PowerShell:
  - Create new profile `user_profile.ps1`
  - Open root powershell, add
    ```shell
    $profile = Join-Path $env:USERPROFILE '\.config\powershell\user_profile.ps1'
    .$profile
    ```
    to assign default powershell with our customized profile (for syncing across devices with Git)
  - Install Scoop: `iwr -useb get.scoop.sh | iex`
  - Install Oh My Posh: `Install-Module oh-my-posh -Scope CurrentUser -Force`
  - Install Terminal Icons `Install-Module -Name Terminal-Icons -Scope CurrentUser -Repository PSGallery -Force`
  - Install z: `Install-Module -Name z -Scope CurrentUser -Force -AllowClobber`
  - Install PSReadLine: `Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck`
  - Install PSFzf: 
    ```shell
    scoop install fzf
    Install-Module -Name PSFzf -Scope CurrentUser -Force
    ```
- Putty: TBU