# DST-Character-Template
Template for starting a Don't Starve Together Character Mod. 

## **DO NOT OVERWRITE THIS FILE! THIS IS MEANT TO BE A STARTING POINT! COPY TO A NEW REPO FOR YOU OWN START!**

Follow along with this [YouTube Video](https://www.youtube.com/watch?v=1lu7rP-U1Zg&t=523s&ab_channel=BunkaHi)

### Steps to take:

1. Download the files and place in either a project directory or the location of the mods for the game
  - ..\Program Files (x86)\Steam\steamapps\common\Don't Starve Together\mods
2. Open up "..\modinfo.lua" and update the file
  - name
  - description
  - author
  - version
  - Search for 'esctemplate' and replace with 'yourcharactername'
```
    - no spaces
    - all lowercase
    - matchcase
    - all subfolders
    - 66 occurrences
```
  - Search for 'ESCTEMPLATE' and replace with 'YOURCHARACTERNAME'
    - no spaces
    - all UPPERCASE
    - matchcase
    - all subfolders
    - 11 occurrences
3. Open the "..\modmain.lua" and update the file
  - '-- The character select screen lines' section
  - '-- The character's name as appears in-game' section
  - '-- Add mod character to mod character list' section
11. Go through all folders and:
  - Replace any 'esctemplate' text with 'yourcharactername' in the file names
  - Replace any 'esctemplate' text with 'yourcharactername' in the folder names
  - Delete any .tex files (associated with images)
  - Delete any .xml files (associated with images)
  - Delete any .zip folders
12. Open up "..\scripts\speech_yourcharactername.lua"
13. Edit any of the dialog you want here
14. Open up "..\scripts\prefabs\yourcharactername.lua"
15. 
