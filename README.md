# Gazebo World Tutorial
## Prepare STL
Open the workspace model in solidworks. Press "save as". Select ".STL" for "save as type"
![saveas](/images/solidworks_saveas.png)

STL is a unitless format. Solidwork exports the dimentions with the default unit of the model file (mm/inch). Gazebo and blender use meter as default unit. To match the unit, click on options,  select meters for unit. Save the STL
![unit](/images/stl_unit.png)

## Texture Mapping
Create a new project in Blender. Delete all existing objects. Import the workspace model by import STL. Orient the obejct properly using the transform field.  

![transform](/images/transform.png)

Go to the uv editing tab

![](/images/uv_editing.png)

unwrap the mesh with smart uv project

![](/images/uv_unwrap.png)

you should see the uv map on the left hand side

![](/images/uv_map.png)

load the desired texture image
![](/images/loadtexture.png)

![](/images/loadtexture2.png)

Go to material properties tab
![](/images/settexture.png)

add new material 
![](/images/settexture2.png)

