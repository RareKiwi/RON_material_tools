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
4. 