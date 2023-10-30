# Gazebo World Tutorial
## Table of Contents  
1. [Prepare STL](#Prepare-STL)
2. [Texture Mapping](#Texture-Mapping)

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

go to base color and click on the circle

![](/images/settexture3.png)

select image texture

![](/images/settexture4.png)

Drop down the image icon, select the image we just loaded 

![](/images/settexture5.png)

Switch to object mode

![](/images/settexture6.png)

change shading to material preview, now the texture should be shown in the rendering 

![](/images/settexture7.png)

export the file as DAE

![](/images/export.png)

## Gazebo Set Up