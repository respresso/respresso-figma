# Export assets from Figma

## Introduction
[Respresso](https://respresso.io) is a digital asset handler, which automatically transforms and delivers assets into your project. Digital assets, such as: localiazion strings, images, colors, app icons. Now, we created an integration tool for you to export easily your assets from [Figma](https://www.figma.com) to [Respresso](https://app.respresso.io). Attention, you cannot import these assets from Respresso to Figma. OK, let see how to use it.

## Integration settings
 
#### Server address
	
 Basically, it is https://app.respresso.io. Change this address if you have an own Respresso server.
 
#### Integration token
	
Respresso has integration token for import data from outside tools. This token isn't same with your project token. You will find this token in path of Poject settings/Integration options.
	
#### Export mode
This is a simple option to choose a comfortable way of the exportation. You can export all of your artboards or only the selected items.
	
#### Localization
Plugin will exports your localization texts if you leave the tick in the rect. This texts have a key and value pair inside Figma. Value is a simple text that you can write into a textbox. Key is complicated than value. You will find this under Layers tab. Click on the textbox and check the Layer tab. In that you can modify the key with a double click on the textview with a T symbol. Respresso suggests a key usage like these:
	
* section.name_of_the_function.name_of_element (main.menu.log_out)
* section_name_of_the_function_name_of_element (main_menu_log_out)
* connected_to.function_name_of_element (user.log_out)
* etc.
	
<p align="center"><img src="documentation/keys.png"></p>

Sometimes designer have to modify localization inside the designer tool. We are motivated to help you and for developers that is why you can reimport all of your localization texts. Let see how can we handle it:
 1. Modify the value is the simpliest case. Respresso will follows the modification.
 2. Key modification not acceptable function through export. Respresso will skip this request. 
 3. Remove isn't acceptable as well (through export process).

 Sometimes you would like skip some texts. In that case add this command: *#respresso-ignore* to the text's key field.
	
#### Color
Respresso plugin can export your colors from Color Styles. Export all of your colors from artboards not an option, pleas use Color Styles. Respresso supports solid and gradient colors, although gradient colors will split by parts of colors and Respresso exports them like solid colors. Local Styles support key and value pairs. You can modify the key of the color with double click on the color under Local Styles/Color Style section.

<p align="center">
	<img src="documentation/design.png">
	<img src="documentation/color_set.png">
</p>

Respresso supports the modification of the color. Change the value and reimport the project. Key modification isn't supported. If you leave the key of the color blanket or you try to import a color with existing key (into Respresso) Respresso can change the name of the key. Our small AI makes a prediction to determine the name of the color.
	
#### Image
You can export images with a simple solution. Select an image and add export option under Design section. Inside the export you can choose a zoom option (0.5x, 1x, 2x etc.), suffix and file format. Respresso supports all file formats from Figma but we would like to suggest svg type. Images have keys as well and you can modify it after a double click on the image. After that Figma opens a Layer window and select the item. Suffix value will place the end of the key. 

<p align="center"><img src="documentation/export.png"></p>
Sometimes an image is splitted by an edge of the artboard inside your design. Respresso will get the original image instead of the splitted one. To avoid this situation use the Clip content possibility among artboard Frame settings. To find this option select the artborad and look at the Design tab. Image modification is fully supported.
	
#### App Icon
Create your app's icon(s) in Figma. Respresso plugin supports Simple and Background - Foreground icons. To import app icons into Respresso you have to use specific keys for images.
* Singe icon key: App icon single
* Background icon: App icon background
* Foreground icon: App icon foreground

Modification is supported as well.

## Integration config

Configuration windows shows basic information about a team and project. You can select a version for each digital asset, which was selected previously. 

## Change Log

Change log contains all modification (create or update) about the project. This may help you to follow the import process.