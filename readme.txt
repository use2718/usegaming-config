	
   Useconfig contains 3 parent folders;
		Config in which all the customizations reside
		Other which has the necessary files for the customizations to work properly
        Screenshots for appearance comparison
	You should check all of them to mish mash whichever config you prefer before deciding

Set Launch Options: 
	-dxlevel 81 (remove this after you launch the game once) -high -console -novid -nojoy -noforcemaccel -nosteamcontroller -noforcemspd 
	-softparticlesdefaultoff -reuse -nohltv -noipx -noforcemaccel -threads (amount of threads your gpu has) -softparticlesdefaultoff 
	-freq (your monitors max refresh rate, if you do not know it is probably 60) -full -w x -h y (desired resolution; e.g 1920x1080) 
	+exec autoexec (optional, will be overwritten if you are already using my config)
		
		Launch options can be accessed via Steam Library > Team Fortress 2 > Properties 

* You can normally squeeze out a few more herts from most 60h monitors, I recommend testing the highest you can go on Nvidia Control Panel before deciding.


* If you dislike the blocky look of the default config:
 write apply_user on console with the autoexec in place (e.g tf\cfg\user\autoexec.cfg) or simply type "mat_filtertextures" and "mat_mipmaptextures" to 1 
	here is a simple one button interchange script;
	
alias matfilteron "mat_filtertextures 1; mat_filterlightmaps 1; alias matfilter matfilteroff"
alias matfilteroff "mat_filtertextures 0; mat_filterlightmaps 0; alias matfilter matfilteron"
alias matfilter "matfilteroff"
bind <key> matfilter

* Nvidia inspector setup guide;

   1. Download and run Nvidia inspector 1.9.5.5 (or simply launch the executable in the folder already provided)
   2. Get the custom file names.xml and put it in the same folder (skip this step if you launched the one in folder)
   3. Click the small icon with 2 tools on it at the right side of driver version (click allow changes)
   4. Navigate to the Team Fortress 2 directory in nvidia inspector from the top left
   5. Import (little green arrow pointing down at box at top right) lodtweak(on) profile (make sure all the compatibility settings are set to the value of hl2/tf2)
   6. Apply changes and Enjoy!
   
If you wish to revert the changes, simply import the lodtweak(off) profile and apply changes.
You will know it works when it shows these lines; 

	Antialiasing - Transparency Supersampling  =  "AA_MODE_REPLAY_MODE_ALL"
	Texture Filtering - LOD Bias  =  "15.000"
	Ambient Occlusion usage  =  "Enabled"
	
 in bold readable text instead of transparent gray.

* If you have an AMD GPU then this method won't work, however there are multiple ways to tweak your level of detail using the Registry Editor, 
or you could watch iMicros detailed guide instead: https://www.youtube.com/watch?v=TdqdpzlsBSk


* Autoexec and Modules go in tf/cfg, all other folders go in custom;

		I suggest you check autoexec.cfg to edit a few binds before launching the game

	*Mounting a VPK to the filesystem is more efficient than adding a subfolder,
as each time the engine needs to open a file, it will need to make a call to the
operating system to search the folder. VPKs can therefore be searched by the engine
much more efficiently. Each subfolder is a new search path that must be checked each
time the engine tries to open a file. So, for optimal load times, always use VPK files
and don't make any subfolders in this folder!

Note that the following directory structure is NOT correct:

	tf/custom/models/my_model.mdl

That will add the directory "tf/custom/models" as a search path, in which case the
file my_model.mdl actually exists at the root of the game's virtual filesystem.
Instead, you would use something like:

	tf/custom/my_custom_stuff/models/my_model.mdl


* When the game boots, this folder is automatically scanned for VPK files or
subfolders. Each subfolder or VPK is added as a search path, so the files
inside those VPK's or subfolders will override the default game files.


* All the mastercomfig addons are self expanatory and completely optional, Included custom files are as follows;
  
    Critical Hit Icon (Can also be used as a directory if you wish to replace it with your own
	Hitsound & Killsound (Can also be used as a directory if you wish to replace them with your own)
	P-rec ( https://etf2l.org/p-rec read prec.info for more info, default set to record all matches) Note; 
		P-rec only works on windows, if you are running linux or mac there is an in game command called ds_enable 1 which is essentially the same thing with less customizations.
	Toon Heart Heal Sign ( Changes healing particles to hearts instead of crosses, also works on sv_pure 1 servers)
	ur_fvms_15_aio ( Stands for user render fixed viewmodels all in one, Fixes more than 400 first person viewmodel animations, most notably soldiers original left hand and spys inspection hands.) 
	smoke (Replaces the explosion effect with spy sapper effect to increase visibility, you can change this script to Muzzle flash/Electric Shock/Pyro Pool on https://cfg.tf)
	Transparent Viewmodels ( Makes your viewmodel see-through, viewmodels block your view, I prefer this to having no viewmodels.) Note; 
		Transparent Viewmodels only work on DirectX Level higher than 90! You can change this setting in launch options.
	Rayshud ( This is a edited 2021 version, i highly recommend replacing this with any of the huds i provided on HUDS Folder, if you wish to see more options you can visit https://huds.tf)
  
  There is already a background for the main menu, if you wish to change this to another image of your choosing you need https://valvedev.info/tools/vtfedit;

  
  1. Find desired background(s) that is high quality 
  2. Open VTFedit, convert your png/jpgs etc. to VTF (you can also use animated backgrounds as well although i dont recommend it due to constant fps drops)
  3. Make sure to check the "No Mipmap" and "No Level of Detail" Flags to not be affected by nvidia inspector
  4. Rename file(s) to;
	background_classic_1.vtf for menu background
	background_upward.vtf & background_upward_widescreen.vtf for normal loading screen (gravelpit also works)
	background_mvm.vtf for MvM mode loading screen
  5. Put files in tf\custom\*any compatible hud*\materials\console
  6. Enjoy!
  
  
		I sincerely hope that this config was satisfactory !

   ⠀⠀      ⣤⡶⢶⣦⡀
⠀⠀⠀⣴⡿⠟⠷⠆⣠⠋⠀⠀⠀⢸⣿
⠀⠀⠀⣿⡄⠀⠀⠀⠈⠀⠀⠀⠀⣾⡿
⠀⠀⠀⠹⣿⣦⡀⠀⠀⠀⠀⢀⣾⣿
⠀⠀⠀⠀⠈⠻⣿⣷⣦⣀⣠⣾⡿
⠀⠀⠀⠀⠀⠀⠀⠉⠻⢿⡿⠟
⠀⠀⠀⠀⠀⠀⠀⠀⠀⡟⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⡟⠀⠀⠀⢠⠏⡆⠀⠀⠀⠀⠀⢀⣀⣤⣤⣤⣀⡀
⠀⠀⠀⠀⠀⡟⢦⡀⠇⠀⠀⣀⠞⠀⠀⠘⡀⢀⡠⠚⣉⠤⠂⠀⠀⠀⠈⠙⢦⡀
⠀⠀⠀⠀⠀⡇⠀⠉⠒⠊⠁⠀⠀⠀⠀⠀⠘⢧⠔⣉⠤⠒⠒⠉⠉⠀ ♥ ⠹⣆
⠀⠀⠀⠀⠀⢰⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢻⠀⠀⣤⠶⠶⢶⡄⠀⠀⠀⠀ ⢹⡆
⠀⣀⠤⠒⠒⢺⠒⠀⠀⠀⠀⠀⠀⠀⠀⠤⠊⠀⢸⠀⡿⠀⡀⠀⣀⡟⠀⠀⠀⠀⢸⡇
⠈⠀⠀⣠⠴⠚⢯⡀⠐⠒⠚⠉⠀⢶⠂⠀⣀⠜⠀⢿⡀⠉⠚⠉⠀⠀⠀⠀⣠⠟
⠀⠠⠊⠀⠀⠀⠀⠙⠂⣴⠒⠒⣲⢔⠉⠉⣹⣞⣉⣈⠿⢦⣀⣀⣀⣠⡴⠟

	
		-Join my discord for feedback!: https://discord.gg/8vhsHtt7RP
		-Check out my twitch!: https://www.twitch.tv/3st_4_D1x
		-If you wish to support me, I accept steam items: https://steamcommunity.com/tradeoffer/new/?partner=1225016958&token=34aMY_rF

			usegaming config v1.02 
			15 March 2022
			
		