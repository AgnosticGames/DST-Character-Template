# DST-Character-Template
Template for starting a Don't Starve Together Character Mod. 

## **DO NOT OVERWRITE THIS FILE! THIS IS MEANT TO BE A STARTING POINT! COPY TO A NEW REPO FOR YOU OWN START!**

Follow along with this [YouTube Video](https://www.youtube.com/watch?v=1lu7rP-U1Zg&t=523s&ab_channel=BunkaHi)
```
Workflow tip: Once the game runs with a new mod, it will compile all the PNGs into the .tex and .xml files along 
with creating the .zip folders (the ones that we will be deleting form the template). Once these have been 
created, you will have to go back and delete them should any PNGs change. This can be mitigated by a few ways:
   - Work in a project directory. When ready, delete the old character mod folder found in the mods directory 
   and copy over the new one from the working project directory.
   - Make it part of your workflow to go through and delete the generated .tex, .xml, and .zip files found 
   inside the character mod folder each time.
   - Make a command script that will do it all for you with a single click (will add one to this template 
   should I get around to it)
I prefer working in a project directory, deleteing old mod folder, and copying new mod folder over because 
this allows the project directory to have version control and when it comes to "publishing" the mod, you will not 
have to worry about any extra .git stuff.
```

### Steps to take:

1. Download the files and place in either a project directory or the location of the mods for the game
   - ..\Program Files (x86)\Steam\steamapps\common\Don't Starve Together\mods
2. Open up `..\modinfo.lua` and update the file
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
```
- no spaces
- all UPPERCASE
- matchcase
- all subfolders
- 11 occurrences
```
3. Open the `..\modmain.lua` and update the file
   - '-- The character select screen lines' section
   - '-- The character's name as appears in-game' section
   - '-- Add mod character to mod character list' section
4. Go through all folders and:
   - Replace any 'esctemplate' text with 'yourcharactername' in the file names
   - Replace any 'esctemplate' text with 'yourcharactername' in the folder names
   - Delete any `.tex` files (associated with images)
   - Delete any `.xml` files (associated with images)
   - Delete any `.zip` folders
5. Open up `..\scripts\speech_yourcharactername.lua` and edit any of the dialog you want here
6. Open up `..\scripts\prefabs\yourcharactername.lua` and edit any of the stats
7. Eidt any of the images that you would like to update for your character
```
Do not change the dimenions of the PNG unless you know what you are doing.
To test your character images out, find the .scml file (..\yourcharactername\exported\yourcharactername), 
right click it, open with, navigate to ..\Program Files (x86)\Steam\steamapps\common\Don't Starve Together Mod Tools
```
