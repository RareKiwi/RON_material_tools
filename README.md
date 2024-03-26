# Ready or Not Material Tools Editor Utility Widget
![](/readme_images/MaterialTools.jpg)  
Tools used to make my [RON materials](https://github.com/RareKiwi/RONmaterials)  
That repo of materials requires you to import textures using this tool. (+ ~50GB project size)

## Umodel texture export instructions
(~130GB preferably SSD space required temporarily)
1. Grab the latest version of the umodel [extract fix](https://www.nexusmods.com/readyornot/mods/666?tab=files&file_id=10974) for RON, and place it with your game pak files. This will prevent umodel crashing during export by replacing certain uassests with empty ones. Remove the pak after you are done to prevent game issues.
2. Open umodel_64 and set the correct settings. You can set the view/export types to texture only. You should untick lightmaps.
3. Set your `Tools > Options: Export location` to an SSD location prefereably with 130GB+ of free space. Not using an SSD can make this and future imports steps take many hours. Enable "Don't overwrite..." in case your umodel crashes.
4. Use `Tools > Scan Content` then switch to `Flat View`
5. Sort by `"Package Name"` then `"Tex"` so Tex:1 is sorted on top. Add .uasset to `"Filter:"` to hide .umaps etc
6. Find the first texture to export. You can skip engine/plugin directories, so start from `/Game/...`
7. Scroll down and shift-click to select the last `Tex = 1` in `/Game/...` and everything in between.
8. Right-click and export
 
## Widget usage for importing Textures:  
> This tool by default filters (excludes) character, item textures and a few other directories from importing as it is map making focused.  
> RONmaterials was initiated without those textures, so any materials or instances will be missing those reference links.  
  
1. Download this repo as a .zip  
> Code - Download Zip  
2. Copy the folders `Content` and `Saved` to your project `...\ReadyOrNotYOURPROJECT\` so that it merges with the existing folders.  
> For example you'd end up with `...\ReadyOrNotYOURPROJECT\Content\Mods\KiwiCode\Builder\EUW_MaterialTools.uasset` etc  
3. Either:  
    * a) Right-Click > Run the EUW_MaterialTools editor widget within UE4 and set the `TGA content path:` to your specific `/game` umodel export directory with the correct forward slashes
	* b) Edit EUW_MaterialTools and change the `Text` value of `EditableTextBox_tgaPath` permanently to your specific `/game` umodel export directory with the correct forward slashes, then compile and save the widget and Right-Click > Run it
> ![](/readme_images/UE4Editor_Q0sojPzfG9.jpg)  
> ![](/readme_images/uhh0zrghs1.jpg)  
4. Click on `Read Textures`  
> This reads `...\ReadyOrNotYOURPROJECT\Saved\SaveGames\HarvestInfo\TextureInfo.sav` which has the texture path and settings saved from the game.
5. Click on `Sort Textures`. Keep the editor focused for max speed.  
> ![](/readme_images/UE4Editor_UpHjIFE5hd.jpg)  
6. Set the `Folder index range` Max value to >= the number of folders or a smaller amount to reduce the number of folders to import at a time if you have low system RAM (<64 GB)  
> If you have < 64GB of RAM (or even more than that honestly) you can do the importing in parts so you can restart the editor in-between to free up RAM.  
> The import can be safely re-run over the same folders, as it should skip existing files.  
> For example if you have 16GB RAM, limiting the range to 0 to 500 every time should get you through the ~2500 folders with 5 restarts.  
7. You should be able to now run `> Import Folders`
> ![](/readme_images/UE4Editor_lXiYVGhezs.jpg)  
8. Repeat steps 3a/4 > 7 if you need to restart the editor to free memory, until all textures are imported.
