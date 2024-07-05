## Steps to creating/editing a map/world in Reforger: 

- Download and install Arma Reforger Tools 
- Download and install Arma Reforger (game) and update to latest game version 
- Open Arma Reforger, go to workshop and download mods that you want to use, explore or edit. 
> These will be downloaded in `Documents > My Games > ArmaReforger > addon`

Start up Arma Reforger Tools. Close it. This will create another directory now in `Documents > My Games > ArmaReforgerWorkbench ..`
> This will have the same directory structure as the ArmaReforger (game), with `addon, logs, profile, your_project_name`.  

Once you have downloaded mods you want to explore, then go to the game `addon` directory and copy them over to the `addon` directory found in `ArmaReforgerWorkbench > addon`. 
> You can add as many mods as you like in this directory and they will automatically show up as an option to load them as dependencies in your project. 

Open up Arma Tools (ArmaReforgerWorkbench) application. Create a new project, name it something informative and avoid spaces. Make sure to select mod dependencies at this stage you want loaded in. 

### Arma Reforger directory structure and naming is important so familiarize yourself with the `ArmaReforger` directory and sub-directories. 

You want to keep a similar schema when developing your own world. NOTE: this will serve as your primary directory where you'll load in game logic and `Prefabs` into your world. `Prefabs` contains __pre-made__ `Prefabs` with all the game logic you will need (pick, drag and drop) into your world. 
See: https://community.bistudio.com/wiki/Arma_Reforger:General_Game_Mode_Setup

With Arma Reforger Tools open, you'll see your `project_name_folder` and all the loaded in mod folders `RHSStatusQuo, etc` .  Next create a working directory structure in your `project_name_folder`.  Click on your `project_name_folder`, hover your mouse to the window below the directory structure window, right-click, create new folder and make at minimum the following two sub-directories `worlds`, `images`. 

You should have the following directory structure now: 
```
-project_name_folder 
--worlds
--images 
```
For testing changes locally, I would highly recommend loading in a smaller, empty world, like `EmptyArland.ent`. 

Next you need to load a world from the `ArmaReforger` directory (the first directory in your directory window, top left). Navigate to `ArmaReforger > worlds > Arland > double-click on EmptyArland.ent`. This will load the Arland world with no structures. 

Next you need to create a `sub-scene (of current World)`  to allow you to make changes to it. With the world loaded in, select File > New World > save it in `project_name_folder > worlds`. 

At this point, you can rename the `default` layer to something like `logic` or `game_mode` layer.  Right-click, rename. You can have multiple layers to separate your `Prefabs`. This is helpful when you want to create a custom mission or scenario. 

Now you are ready to load in pre-made `Prefabs` for factions, arsenals, game modes, etc. You can search for these by name and just drop them into your world. The base ones listed below doesn't matter where you drop them. They just tell the game, these are the "settings for factions, arsenals, and AIs". 
See: https://community.bistudio.com/wiki/Arma_Reforger:General_Game_Mode_Setup

At minimum, you need to load in the following `Prefabs`: 
They are all found under: `Prefabs > MP > ..`
1. `GameMode_Plain.et`: needed to pre-load all the `Prefabs` for the game to function. 
> You can rename it from `GameMode_Plain1` to `GameMode_GM` for game master. 
2. `FactionManager_USxUSSR1.et`: needed to select Factions 
3. `LoadoutManager_USxUSSR.et`: needed for US/RUS loadouts. 
4. `LoadoutManager_USMCxMSV.et`: needed for RHS loadouts USMC and MSV. 
> Note this was grabbed from the `RHSStatusQuo > MP > Managers >  Loadouts`.

You must load these in for AI to function properly in-game:  
This is found under  `Prefabs > World > Game`. 
5. `PerceptionManager.et`: needed for AI behavior.
This is found under  `Prefabs > World > AI`. 
6. `SCR_AIWorld.et` : this controls the navmesh for the AI. 
> May need to load in world specific navmes here, for example, `SCR_AIWorld_Eden`. TBD. 


