# Gazebo World Tutorial
## Table of Contents  
1. [Prepare STL](#Prepare-STL)
2. [Texture Mapping](#Texture-Mapping)
3. [Gazebo Setup](#Gazebo-Setup)
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

## Gazebo Setup

Go to the home directory of your ros machine, select show hidden files 

![](/images/gazebo1.png)

Find ".gazebo" folder 

![](/images/gazebo2.png)

Create new folder, name it "models"

![](/images/gazebo3.png)

Put the DAE file and the texture image in the models folder

![](/images/gazebo4.png)

Create a folder named worlds in your package, create the world file in it.

![](/images/gazebo5.png)

point the mesh model and collision model to "model://[MODEL NAME]". the "model://" path is default to the models folder we created earlier. 

![](/images/gazebo6.png)

make a launch file that launch the world we created

![](/images/gazebo7.png)

roslaunch it and the model with texture should be showing up

![](/images/gazebo.png)
