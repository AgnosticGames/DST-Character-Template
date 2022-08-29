# DST-Character-Template
Template for starting a Don't Starve Together Character Mod. 

## **DO NOT OVERWRITE THIS FILE! THIS IS MEANT TO BE A STARTING POINT! COPY TO A NEW REPO FOR YOU OWN START!**

Follow along with this [YouTube Video](https://www.youtube.com/watch?v=1lu7rP-U1Zg&t=523s&ab_channel=BunkaHi)  
[This](https://www.lua.org/start.html) is a good place to learn LUA from the beginning  
[This](http://tylerneylon.com/a/learn-lua/) is also a good source to brush up on LUA programming  
[This](https://www.tutorialspoint.com/execute_lua_online.php) is a nice place to practice LUA programming  
[This](https://forums.kleientertainment.com/forums/topic/116302-ultromans-tutorial-collection-newcomer-intro/) is a great place to start to learn the breakdown of mods
[This](https://forums.kleientertainment.com/forums/topic/128108-where-are-mods-stored-now/) is where to find the API V2 mods

You can also download other mods and look through them and see how others have created their mods as well.  
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
   - ..\Program Files (x86)\Steam\steamapps\workshop\content\322330\  <- NEW V2 LOCATION FOR WORKSHOP FILES
2. Open up `..\modinfo.lua` and update the file
   ```
   This is where the main discriptions of the mod and mod options are found/created
   ```
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
   Do not change the dimenions of the PNG unless you KNOW what you are doing.
   To test your character images out, find the .scml file (..\exported\yourcharactername), 
   right click it, open with, navigate to 
   ..\Program Files (x86)\Steam\steamapps\common\Don't Starve Together Mod Tools\mod_tools\spriter\spriter.exe
   Do not save anything in this file unless you KNOW what you are doing. This is mostly to test your edits 
   without having to launch the game
   ```
   - If you want a part of the mod to be 'invisable', navigate to `..\exported\yourcaractername_cleared\folder of part`
   and copy the images found there. Then navigate to `..\exported\yourcaractername\folder of part` and delete the
   orignial images and paste the copied ones into that folder. Open the `.scml` file again and see the change
    
### API
In order to get an "API" to kinda work as you build your mod, you will have to take a few extra steps. Word of caution:  
this will add a TON of files (3,000+) to your workspace and your repo if you are working with one. Keeping track of all  
of your mod files will become very difficult. A possible recommendation is to make two seperate project directory. One  
that holds all of the game scripts and mod files that will be written over multiple times and one that will only hold  
the mod files that will be pushed to version control and the community mod page. This should be set up first before  
starting your mod files because they will share some of the file locations (scripts is the big one). The scripts will not  
be added to this template due to the version of the game that could be out.  

1. You can use Visual Studio + lua IntelliSense or download IntelliJ IDEA Community + Emmy LUA Plugin
   - Follow along [here](https://dst-api-docs.fandom.com/wiki/Tools)
2. You will need to grab the `.zip` file from `..\Program Files (x86)\Steam\steamapps\common\Don't Starve Together\data\databundles\scripts.zip`
3. Extract the files in the location where you will be working on your project mod
4. Download the template files and complete the renaming steps
5. Transfer the template files into the project directory where you unzipped the files from Don't Starve Together
   - These will have a similar directory structure. You will see similar files in the same place. A good one to look 
   for first is the speech files
6. You should now have it set up where you can use an IntelliSense to help auto fill names and look at the files they 
are from to learn how they are used
