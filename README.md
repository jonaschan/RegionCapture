# Texture Region Capture (Ver. 2.0)
Plugin for Unity 2017.2 and higher

Compatibility with Vuforia 6.5 - 7.X
 (ARCore and ARKit - Coming soon)

![Region Capture description](https://raw.githubusercontent.com/maximrouf/RegionCapture/master/Images/RegionCapture.jpg)

How to setup:

	1. Start a new Unity project

	2. Open the Layers-tab in "Project settings -> Tags and Layers" and set the "Layer №20" name as "Region_Capture" 

	3. Go to "Project settings -> Player" and select the "XR Settings -> Vuforia" checkbox

	4. Then click in the upper menu to "GameObject -> Vuforia -> ARCamera" (to import Vuforia files into the project)

	5. Now you can import the "RegionCapture_2.0.unitypackage" into your project

	6. Select "Resources -> VuforiaConfiguration" in the "Project View" and paste your licence key in the upper field

	7. Also you need to enable "Load StonesAndChips" checkbox in the "Datasets" rollout and click "Activate"

	8. Run the demo-scenes into "Assets -> Region_Capture -> Examples"


How to use:

	1. Set the custom Scale, Position and Rotation to modify region-size
	
	2. Get Texture from "Render_Texture_Camera" in "PlayMode" - RenderTextureCamera.GetRenderTexture()

	3. Enable the option - "Check if the plane is out of bounds" on the "RegionCapture" GameObject 
	   to get the some scripted Unity Events, if the capturing plane is out of a Camera bounds

	4. If all works fine - switch off Layer "Region_Capture" in : ARCamera -> Camera -> Culling Mask 
	   (or enable the "Hide this layer from ARCamera" checkbox);


Available methods:

	Region_Capture.RecalculateRegionSize();		//  Call it - if the marker has changed

	RenderTextureCamera.RecalculateTextureSize();	//  Call it - if the marker or size of renderTexture has changed

	RenderTextureCamera.MakeScreen();		//  Call it - if you want to save RegionTexture to localStorage


  Best Regards, Maxim Rouf
