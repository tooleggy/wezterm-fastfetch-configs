# My Wezterm and FastFetch configs

## 📷
<img width="2474" height="965" alt="image" src="https://github.com/user-attachments/assets/12b8e756-3132-4595-b6f3-3ec83261802d" />


## Installation
(Note I will give the powershell for wezterm & fastfetch installations, if you are not comfortable using cli you can look up the installations from google)

### Installing Wezterm
Open powershell and run
```
winget install --id wez.wezterm --exact
```
This will install wezterm

### Installing fastfetch
Open powershell and run
```
winget install Fastfetch-cli.Fastfetch   
```
Once fastfetch is installed you can run
```
fastfetch --gen-config
```
to create the .jsonc file for configuration

## Adding the configs for Wezterm and fastfetch
### Wezterm
Locate you Users folder for Wezterm, and either create or add my file
```
"C:\Users\{USERNAME}\.wezterm.lua"
```
This is the default lua script via Wezterm documentation, if you would like to config it on your own
```
-- Pull in the wezterm API
local wezterm = require 'wezterm'

-- This will hold the configuration.
local config = wezterm.config_builder()

-- This is where you actually apply your config choices.

-- For example, changing the initial geometry for new windows:
config.initial_cols = 120
config.initial_rows = 28

-- or, changing the font size and color scheme.
config.font_size = 10
config.color_scheme = 'AdventureTime'

-- Finally, return the configuration to wezterm:
return config
```

### fastfetch
your fastfetch script will download by default once you run the command, the file path will be:
```
C:\Users\{USERNAME}\.config\fastfetch
```
You can replace it with my config, or start your own from this file
For my ASCII art logo, add the logo.txt file from this repo

## Finishing touches
Once you have installed these at the proper place, you should be able to open and run wezterm, with this config, and run fastfetch to get your desired fastfetch info.
