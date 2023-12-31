# RoN Material Tools Editor Utility Widget

## Umodel texture export instructions
0. TBD
 
## Widget usage for importing Textures:  
1. Download this repo as a .zip  
> Code - Download Zip  
2. Copy the folders `Content` and `Saved` to your project `...\ReadyOrNotYOURPROJECT\` so that it merges with the existing folders.  
> For example you'd end up with `...\ReadyOrNotYOURPROJECT\Content\Mods\KiwiCode\Builder\EUW_MaterialTools.uasset` etc  
3. Either:
    * a) Right-Click > Run the EUW_MaterialTools editor widget within UE4 and set the `TGA content path:` to your specific `/game` umodel export directory with the correct forward slashes
	* b) Edit EUW_MaterialTools and change the `Text` value of `EditableTextBox_tgaPath` permanently to your specific `/game` umodel export directory with the correct forward slashes, then compile and save the widget and Right-Click > Run it
> ![](/readme_images/uhh0zrghs1.jpg)
4. Click on `Read Textures`
> This reads `...\ReadyOrNotYOURPROJECT\Saved\SaveGames\HarvestInfo\TextureInfo.sav` which has the texture path and settings saved from the game.
5. Click on `Sort Textures`. Keep the editor focused.
6. Set the `Folder index range` Max value to >= thenumber of folders or a smaller amount to reduce the number of folders to import at a time if you have low system RAM (<64 GB)  
>> If you have < 64GB of RAM (or even more than that honestly) you can do the importing in parts so you can restart the editor in-between to free up RAM.  
>> The import can be safely re-run over the same folders, as it should skip existing files.  
>> For example if you have 16GB RAM, limiting the range to 0 to 500 every time should get you through the ~2500 folders with 5 restarts.  
7. Run `> Import Folders`
8. Repeat steps3/4 > 7 if you need to restart the editor to free memory, until all textures are imported.