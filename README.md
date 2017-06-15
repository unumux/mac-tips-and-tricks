# Unum UX Mac: Tips and Tricks for FEDs
A small collection of tips and tricks for Mac FEDs. This is just a collection of notes for my presentation, so some of these things may not make sense on their own. 

# General Mac Tools/Tips
- Brief intro to how macs handle apps vs windows

## Gestures: 
- 3 finger up: show all windows and spaces
- 3 finger down: show windows for currently active app
- 3 finger swipe: show other spaces
- 4 finger expand - show desktop
- 4 finger pinch: show launchpad
- while hovering over app in dock - 2 finger swipe up; show windows for app

## Special Keyboard Keys
- ⌘ is the Command/Cmd () key
- ⌃ is the Control/Ctrl/Ctl key
- ⌥ is the Option/Opt (alt) key
- ⇧ is the Shift key
- fn is the Function key

## Keyboard shortcuts
- Cmd+Q: Quit app
- Cmd+W: Close window
- Cmd+Opt+W: Close all windows for app
- Cmd+M: Minimize window
- Cmd+H: Hide app (not minimize)
  - fade app in dock: defaults write com.apple.Dock showhidden -boolean yes; killall Dock
- Cmd+Tab: App switcher
- Cmd+` (tilde): Window switcher in current app
- Cmd+Space: Alfred OR Spotlight
- Cmd+,: Preferences, in most apps

## Other tips
- MacOS Dragging
- Stacks
- Spacebar quick look

## Recommended Apps
- Trailer App: https://ptsochantaris.github.io/trailer/
- Dock spacers: https://github.com/chuckhendo/add-dock-spacer
- Window managers: 
    - Magnet: 0.99 on App Store: http://magnet.crowdcafe.com/
    - Spectacles: Free: https://www.spectacleapp.com/
- Alfred: https://www.alfredapp.com/
    - Clear your clipboard before demonstrating :)
    - Cmd+Shift+C: Clipboard history
    - File system browsing
    - Workflows!
- Git GUIs (trigger warning)
    - Sourcetree: https://www.sourcetreeapp.com/ (stupid buggy, but powerful and free)
    - Github Desktop: https://desktop.github.com/ (kinda slow, limited functionality, free)
    - Tower: https://www.git-tower.com/mac/
    - Visual Studio Code


# zsh
- nvm: https://github.com/creationix/nvm
- Homebrew: https://brew.sh/
- Cask: https://caskroom.github.io/ (undecided on whether to use this)
- iTerm vs bash vs zsh vs oh-my-zsh
    - Big difference between zsh and bash - powerful autocompletion
    - Other shells
        - cmd.exe
        - PowerShell (now available on Mac)
    - oh-my-zsh
        - demonstrate tab completion
        - Themes (more than just colors): https://github.com/robbyrussell/oh-my-zsh/wiki/Themes
        - Plugins (may increase load time): https://github.com/robbyrussell/oh-my-zsh/wiki/Plugins
- Git vs Github
    - Git is a standalone thing from Github
    - We could use Git without Github altogether by: 
        - Using TFS Git, Bitbucket, or Gitlab (among many, many others)
        - Connecting directly to a "remote" repo
        - Just using it locally and never pushing
    - Github provides access control and collaboration features
- Git shortcuts in oh-my-zsh: https://github.com/robbyrussell/oh-my-zsh/wiki/Plugin:git
    - Ones I typically use: 
        - `ga .` (git add .)
        - `gc -m "commit message"` (git commit -m "commit message")
        - `gp` (git push)
        - `gcb branch-name` (git checkoub -b branch-name) - create a new branch
        - `gco branch-name` (git checkout branch-name) - checkout existing branch
- Github Hub: https://github.com/github/hub
    - hub create
    - hub clone
    - hub browse
- open command
- take command
- iTerm profiles!
- alias co=“code .”
- dot files
    - .zshrc
    - https://dotfiles.github.io/

# VSCode
- Start here: https://github.com/Microsoft/vscode-tips-and-tricks
- Interactive Playground: Help -> Interactive Playground
- Command Palete: cmd+shift+p
- Terminal: ctrl+` (tilde)
- Icon Themes
    - Cmd+Shift+P->icon->Preferences: File Icon Theme
    - I use Material Icon Theme
    - Seti is another good option
- Key chords: 
    - Change language mode: cmd+k m (hit cmd+k, and THEN m)
    - usually (always?) start with CMD+K
- Keybindings: cmd+shift+p->keyboard->Open Keyboard Shortcuts
    - Keybindings that I use:
    ```
    [
        {
            "key": "shift+cmd+g",
            "command": "workbench.view.scm"
        },
        {
            "key": "shift+cmd+r",
            "command": "workbench.action.tasks.runTask"
        },
        {
            "key": "cmd+r",
            "command": "workbench.action.debug.start",
            "when": "!inDebugMode"
        },
        {
            "key": "cmd+r",
            "command": "workbench.action.debug.restart",
            "when": "inDebugMode"
        }, 
        {
            "key": "shift+cmd+s",
            "command": "git.sync"
        }
    ]
    ```
- Settings: Global vs Workspace
    - Global: Access with Cmd+,
    - Some useful global settings
        - `"explorer.openEditors.visible": 0,`
        - `"git.confirmSync": false`
        - `"editor.fontFamily"` & `"editor.fontSize"` & `"editor.fontWeight"`
        - `"git.enableSmartCommit": true`
- Emmet
    - Set "emmet.useNewEmmet": true
    - HTML
        - .my-class>.child-class{Content}+.child-sibling{Content 2}
        - .my-class>.child-class*5
        - .my-class>.child-class-${Content $}*5
        - ul.list>li.list-item*5>Lorem
    - SCSS/CSS
        - db / df
        - p15
        - mt10+mb10
        - p15p
        - df+fg1+fb100p

## Extensions
- Install going to the extensions pane, searching for `chuckhendo` and installing `chuckhendo-vscode-extensions`
- List
    - Advanced New File: cmd+option+n  (may want to change some settings)
    - Annotator: show who modified lines in a git repo
    - Auto Close Tag: If you're not using emmet for whatever reason (maybe using css intellisense), this autocloses tags
    - Code Runner: Run bits of code, including individual lines
    - Debugger for Chrome: debug scripts running in Chrome. Doesn't currently work with Oak :(
    - Git History: Visual Git log
    - gitignore: Right click to add files/folders to .gitignore file
    - IntelliSense for CSS class names: autocompletion of all css classes in your project
    - NPM Intellisense: autocompletion for NPM packages
    - Path Intellisense: autocompletion for path names
    - Willow Snippets: :)

# Finding new stuff
- Follow Matt Smith on Github! https://github.com/allthingssmitty and http://allthingssmitty.com/ 
- Look for "awesome" lists on github
    - https://github.com/jaywcjlove/awesome-mac
    - https://github.com/viatsko/awesome-vscode
- Reddit
    - https://www.reddit.com/r/macapps/
    - https://www.reddit.com/r/vscode/
    - https://www.reddit.com/r/zsh/
- Hacker News: https://news.ycombinator.com/
- Twitter
    - https://twitter.com/code
- Wes Bos's Command Line Power User: https://commandlinepoweruser.com/ 
    - Free, and just over an hour long

