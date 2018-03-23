# dot-files

### The following repos/ dotfiles played a very important role in the creation of this dotfile

* Dotbot: https://github.com/anishathalye/dotbot
* Dotfiles using Dotbot: https://github.com/magicmonty/dotfiles_dotbot
* https://github.com/Vaelatern/init-dotfiles
* https://github.com/anishathalye/dotfiles_template


# Dotfiles

Dotfile management using [Dotbot](https://github.com/anishathalye/dotbot).
Structure of this repository is strongly inspired by [vsund](https://github.com/vsund/dotfiles) and [vbrandl](https://github.com/vbrandl/dotfiles).

## Screenshots

Screenshots are in the [Wiki](https://github.com/magicmonty/dotfiles_dotbot/wiki)

## Dependencies

* git
* ruby
* node
* nvim / vim (depending of profile)
* homebrew (in osx)
* tmux
* fish

## Installation

```bash
~$ git clone --recursive https://github.com/magicmonty/dotfiles_dotbot .dotfiles
```

For installing a predefined profile:

```bash
~/.dotfiles$ ./install-profile <profile> [<configs...>]
# see meta/profiles/ for available profiles
```

For installing single configurations:

```bash
~/.dotfiles$ ./install-standalone <configs...>
# see meta/configs/ for available configurations
```

You can run these installation commands safely multiple times, if you think that helps with better installation.

### Mutt / MSMTP / offlineimap

For this to work correctly, you have to add the following entries to the login keychain:

| Name                   | Account name       | Source                                                       |
|------------------------|--------------------|--------------------------------------------------------------|
| imap.google.com        | the IMAP user name | Application Passwort (create in https://accounts.google.com) |
| smtp://smtp.google.com | the SMTP user name | Application Passwort                                         |

### Mates / vdirsyncer

for the address book to work correctly you have to add the following entries to the login keychain:

| Name                | Account name  | Source                                                                            |
|---------------------|---------------|-----------------------------------------------------------------------------------|
| calendar.google.com | client_id     | Client id from project in https://console.developers.google.com (CardDAV API)     |
| calendar.google.com | client_secret | Client secret from project in https://console.developers.google.com (CardDAV API) |

## License

This software is hereby released into the public domain. That means you can do
whatever you want with it without restriction. See `LICENSE` for details.

## Contents

### Profiles

```
meta/profiles
├── linux
├── macosx
└── windows10
```

### Configs

```
meta
├── base.json
└── configs
      ├── apt.linux.json
      ├── apt.windows10.json
      ├── dev.json
      ├── emacs.json
      ├── fish.linux.json
      ├── fish.osx.json
      ├── fish.windows10.json
      ├── git.json
      ├── git.np4.json
      ├── go.json
      ├── homebrew.json
      ├── mutt.osx.json
      ├── node.json
      ├── osx_defaults.json
      ├── profanity.json
      ├── ruby.json
      ├── sonic-pi.json
      ├── spectacle.json
      ├── ssh.json
      ├── sublime.json
      ├── tmux.linux.json
      ├── tmux.osx.json
      ├── vim.linux.json
      ├── vim.osx.json
      ├── vim.windows10.json
      └── vscode.json
```

### Dotfiles

```
.
├── Brewfile
├── apps
│  ├── OSXTerminal
│  │  ├── Gruvbox-Dark.terminal
│  │  └── Solarized Dark.terminal
│  ├── SublimeText
│  │  └── Preferences.sublime-settings
│  ├── VSCode
│  │  ├── keybindings.json
│  │  └── settings.json
│  ├── iterm2
│  │  ├── Solarized Dark.itermcolors
│  │  ├── Solarized Light.itermcolors
│  │  ├── com.googlecode.iterm2.plist
│  │  └── gruvbox-dark.itermcolors
│  ├── mutt
│  │  ├── _bin
│  │  │  └── html2text.py
│  │  ├── msmtprc
│  │  ├── mutt
│  │  │  ├── accounts
│  │  │  │  ├── all
│  │  │  │  ├── familie
│  │  │  │  └── pagansoft
│  │  │  ├── alias
│  │  │  ├── colors
│  │  │  │  ├── gruvbox-16.muttrc
│  │  │  │  └── gruvbox-256.muttrc
│  │  │  ├── contacts-filter.sh
│  │  │  ├── gpg.rc
│  │  │  ├── mailcap
│  │  │  ├── offlineimap.py
│  │  │  ├── quote-html-message.sh
│  │  │  └── view_attachment.sh
│  │  ├── muttrc
│  │  ├── offlineimaprc
│  │  └── vdirsyncer_config
│  ├── notmuch
│  │  ├── notmuch-config
│  │  └── notmuch-py
│  │     ├── AUTHORS
│  │     ├── LICENSE
│  │     ├── README.md
│  │     ├── mutt-notmuch-py
│  │     └── setup.py
│  ├── profanity
│  │  ├── icons
│  │  ├── profrc
│  │  └── themes
│  │     └── live
│  ├── sonic-pi
│  │  ├── init.rb
│  │  └── snippets
│  │     ├── bow.sps
│  │     ├── echo.sps
│  │     ├── ether.sps
│  │     ├── fx.sps
│  │     ├── gate.sps
│  │     ├── knit.sps
│  │     ├── live_loop.sps
│  │     ├── mountain.sps
│  │     ├── mountainloop.sps
│  │     ├── pitchshift.sps
│  │     ├── reverb.sps
│  │     ├── ring.sps
│  │     ├── rll.sps
│  │     ├── shd.sps
│  │     ├── shdd.sps
│  │     ├── slicer.sps
│  │     ├── smp.sps
│  │     └── wsynth.sps
│  ├── spectacle
│  │  └── spectacle.json
│  ├── ssh
│  │  └── config
│  └── tmux
│     ├── bin
│     │  ├── battery.sh
│     │  └── tmux-mem-cpu-load
│     ├── tmux
│     │  └── solarized
│     │     ├── tmuxcolors-256.conf
│     │     ├── tmuxcolors-dark.conf
│     │     └── tmuxcolors-light.conf
│     ├── tmux.conf
│     ├── tmux.live.conf
│     └── tmuxinator
│        ├── live.yml
│        ├── playground.yml
│        ├── socrates.yml
│        └── wmfra.yml
├── development
│  ├── editorconfig
│  ├── git
│  │  ├── gitconfig
│  │  ├── gitconfig.np4
│  │  └── gitignore_global
│  ├── go
│  │  └── go-version
│  ├── node
│  │  ├── node-version
│  │  └── npmrc
│  └── ruby
│     ├── gemrc
│     └── ruby-version
├── editors
│  ├── emacs
│  │  ├── bin
│  │  │  └── edit
│  │  ├── emacs.d
│  │  │  └── private
│  │  │     └── sonic-pi
│  │  │        ├── README.org
│  │  │        ├── config.el
│  │  │        ├── extensions.el
│  │  │        ├── packages.el
│  │  │        └── snippets
│  │  │           └── sonic-pi-mode
│  │  │              ├── bitcrusher.snippet
│  │  │              ├── distortion.snippet
│  │  │              ├── ll.snippet
│  │  │              ├── ring.snippet
│  │  │              ├── rll.snippet
│  │  │              └── wsyn.snippet
│  │  └── spacemacs
│  └── vim
│     ├── config
│     │  └── nvim
│     │     ├── init.linux.vim
│     │     └── init.osx.vim
│     ├── gvimrc
│     ├── plugins
│     │  ├── plugins_linux.vim
│     │  ├── plugins_osx.vim
│     │  ├── plugins_shared.vim
│     │  └── plugins_windows10.vim
│     ├── vim
│     │  ├── UltiSnips
│     │  │  ├── clojure
│     │  │  │  └── overtone.snippets
│     │  │  └── clojure.snippets
│     │  ├── autoload
│     │  │  └── plug.vim
│     │  ├── ftdetect
│     │  │  └── xaml.vim
│     │  ├── ftplugin
│     │  │  └── fish.vim
│     │  ├── insert_matching_spaces.vim
│     │  ├── map_line_block_mover_keys.vim
│     │  ├── map_option_highlighting_keys.vim
│     │  ├── mkzip.sh
│     │  ├── run-last.vim
│     │  ├── set_abbreviations.vim
│     │  ├── toggle_highlights.vim
│     │  ├── update_visual_highlight_color.vim
│     │  └── vim-fireplace-mappings.vim
│     └── vimrc
├── fonts
│  └── Monoid
│     ├── Monoid Bold Nerd Font Complete.ttf
│     ├── Monoid Bold Nerd Font Complete Mono.ttf
│     ├── Monoid Bold Nerd Font Complete Mono Windows Compatible.ttf
│     ├── Monoid Bold Nerd Font Complete Windows Compatible.ttf
│     ├── Monoid Italic Nerd Font Complete.ttf
│     ├── Monoid Italic Nerd Font Complete Mono.ttf
│     ├── Monoid Italic Nerd Font Complete Mono Windows Compatible.ttf
│     ├── Monoid Italic Nerd Font Complete Windows Compatible.ttf
│     ├── Monoid Regular Nerd Font Complete.ttf
│     ├── Monoid Regular Nerd Font Complete Mono.ttf
│     ├── Monoid Regular Nerd Font Complete Mono Windows Compatible.ttf
│     ├── Monoid Regular Nerd Font Complete Windows Compatible.ttf
│     ├── Monoid Retina Nerd Font Complete.ttf
│     ├── Monoid Retina Nerd Font Complete Mono.ttf
│     ├── Monoid Retina Nerd Font Complete Mono Windows Compatible.ttf
│     └── Monoid Retina Nerd Font Complete Windows Compatible.ttf
├── images
│  ├── lambdaphonic.png
│  ├── man-woman-geek.jpg
│  ├── sheep-desktop.jpg
│  └── tron-legacy-wallpaper-08-2588.jpg
├── install-profile
├── install-standalone
├── macos
└── shells
   └── fish
      └── config
         └── fish
            ├── abbr.fish
            ├── abbr.linux.fish
            ├── abbr.windows10.fish
            ├── autoenv.fish
            ├── completions
            │  └── fisher.fish
            ├── config.fish
            ├── config.windows10.fish
            ├── fishfile.linux
            ├── fishfile.osx
            ├── fishfile.windows10
            └── functions
               ├── edit_config_fish.fish
               ├── fish_greeting.fish
               ├── fish_mode_prompt.fish
               ├── fish_prompt.fish
               ├── fish_right_prompt.fish
               ├── fish_title.fish
               ├── fish_user_key_bindings.linux.fish
               ├── fish_user_key_bindings.osx.fish
               ├── fish_user_key_bindings.windows10.fish
               ├── fisher.fish
               ├── gls.fish
               ├── git.fish
               ├── gitv.fish
               ├── l.fish
               ├── la.fish
               ├── ll.fish
               ├── ls.fish
               ├── m.fish
               ├── mail.fish
               ├── psa.fish
               └── search_history.fish

```
