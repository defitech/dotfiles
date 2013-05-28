# Defitech default dotfiles

OSX, Homebrew, fish, git, Slate.


## Features

- Bootstrap script (`bootstrap.bash`) that syncs dotfiles to home dir, installs latest fish with Homebrew if missing and applies fish settings (universal vars)
- [fish](https://github.com/fish-shell/fish-shell) config (`.config/fish`) including 2-line prompt with user, host, working dir, git status (assumes terminal with dark background); e.g. <br/>
  <img src="http://sgoumaz.github.io/dotfiles/images/prompt-fresh.png" alt="Prompt example (fresh)"/><br/>
  *Experimental hack: The user, host and current working dir parts are dimmed when they don't change for less distraction; e.g.*<br/>
  <img src="http://sgoumaz.github.io/dotfiles/images/prompt-dimmed.png" alt="Prompt example (dimmed)"/>
- [Slate](https://github.com/jigish/slate) settings (minimal for now)
- Homebrew formulae (`brew.bash`)
- OSX settings (`osx.bash`)—need a review

The latter two borrow heavily from @mathiasbynens's [dotfiles](https://github.com/mathiasbynens/dotfiles).


## Installation

Prerequisite: Homebrew.

1. `./bootstrap.bash` (or `./bootstrap.bash -f` to avoid the confirmation prompt)
2. If necessary, add fish to the system shells and make it your default shell:
    - Add `/usr/local/bin/fish` to `/etc/shells`
    - `chsh -s /usr/local/bin/fish`
3. Apply OSX settings if desired: `./osx.bash`
4. Install Homebrew packages if desired: `./brew.bash`
5. Install TextWrangler color scheme if desired: `cp init/Twilight.bbcolors ~/Library/Application\ Support/TextWrangler/Color\ Schemes/.`


## Original source

https://github.com/sgoumaz/dotfiles.
