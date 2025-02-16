# roon-tui

A Roon Remote for the terminal

![Roon TUI screenshot](images/screenshot.png)

## Building from Source Code MacOS X 12.6.7 Monterey in my case.
* `brew install rust` // None-brew-option: Rust: visit [rustup.rs](https://rustup.rs/) and follow the provided instructions
* `cd /opt/local/dev/`
* Clone the roon-tui git repository: `git clone https://github.com/TheAppgineer/roon-tui.git`
* Change directory and build the project: `cd roon-tui && cargo build --release`
* The binary can be found in: `target/release/roon-tui`
* `chmod +x /opt/local/dev/roon-tui/target/release/roon-tui`
* `/opt/local/dev/roon-tui/target/release/roon-tui&`

## Downloading Release Binaries
Prebuilt binaries can be downloaded from the [latests release](https://github.com/TheAppgineer/roon-tui/releases/latest) page on GitHub. Binaries might have been created by other users for platforms I don't have access to myself.

The prebuilt alpha fails for me: `-bash: /Users/user/Downloads/roon-tui: Bad CPU type in executable`

## Authorizing Core Access
On first execution the outside border of the UI will be highlighted without any views active, this indicates that pairing with a Roon Core has to take place. Use your Roon Remote and select Settings&rarr;Extensions from the hamburger menu and then Enable Roon TUI.

## Project Status
This is Alpha stage software. Instead of using the official [Node.js Roon API](https://github.com/RoonLabs/node-roon-api) provided by Roon Labs this project uses an own developed [Rust port](https://github.com/TheAppgineer/rust-roon-api) of the API.

## Key Bindings
### Global (useable in all views)
|||
|---|---|
|Tab|Swith between views
|Ctrl-z|Open zone selector
|Ctrl-p|Play / Pause
|Ctrl-c|Quit
### Common list controls
|||
|---|---|
|&uarr;|Move up
|&darr;|Move down
|Home|Move to top
|End|Move to bottom
|Page Up|Move page up
|Page Down|Move page down
### Browse View
|||
|---|---|
|Enter|Select
|Esc|Move level up
|Ctrl-Home|Move to top level
|F5|Refresh
### Queue View
|||
|---|---|
|Enter|Play from here
### Now Playing View
|||
|---|---|
|m|Mute
|u|Unmute
|+|Increase volume
|-|Decrease volume
### Search Popup
|||
|---|---|
|Enter|Search provided term
|Esc|Back to Browse view
### Zone Select Popup
|||
|---|---|
|Enter|Select Zone
|Esc|Back to previous view

# User experience
I now have `Roon TUI` running on Solus Budgie Desktop, I installed both the rust packages, namely `Rust` and `Rustup`, then did the following in terminal:
```Sh
cd /opt/local/dev
git clone https://github.com/TheAppgineer/roon-tui
cd roon-tui
cargo run
```
