# blender-matcap generator
 Blender generator for MatCaps / "Sphere Textures".

 This is a generator for Matcap textures using a combination of various lighting setups, including 'shadow lights' which remove light, and Blender's material node setup.
 
 Basic materials have been added, but it is compatible with any node groups that can be applied to a basic UV Sphere.
 
## Installation

Both a raw .blend file and a startup file have been included. I *highly* suggest using the startup file - you can install it as seen here:
![image](https://user-images.githubusercontent.com/80061436/114399295-ab86bb00-9b98-11eb-892f-81cc274fc089.png)

This will mean that you can access the initial file at any time. It will *not* replace your initial startup file, it simply adds a new workspace you can select on a new project - meaning you can experiment with the file and return to the inital state of the generator when required. 

### If you wish to override the inital generator file (perhaps you've added materials or lighting setups, etc), you can unzip the MatcapGen.zip and overwrite the startup.blend with your new file. **Make sure the filename remains to be startup.blend - rename it if necessary**
You can then rezip and overwrite the original by running the Install Application Template again:
![image](https://user-images.githubusercontent.com/80061436/114399934-61eaa000-9b99-11eb-9fb9-ac50889b0b49.png)



 ### Tutorial

Usage is simple - arrange lights and material as desired, then render the Viewport as using Viewport Render Image! (ctrl + ;)

*Follow the built in Text Editor instructions to ensure your material preview is setup correctly!*

If you add or create a material, make sure it is marked as having a Fake User:![image](https://user-images.githubusercontent.com/80061436/114400322-bd1c9280-9b99-11eb-98a6-fde13cea0a1f.png)

This will ensure it will not be removed if it is not currently in use.

## Material and Lights

This workspace is the main scene where you have direct access to the Material for the sphere that generates the Matcap.
You also have access to a variety of preset lights. These *will* react differently depending on your material setup - some sun lights set up as rim lights will be *VERY* powerful with certain materials. Be warned.

Notes and preview here:
![image](https://user-images.githubusercontent.com/80061436/114403796-03272580-9b9d-11eb-8ced-237762d31c4e.png)

## Image Input Node

This workspace allows you to easily input an image to be used as a HDRI for the scene. This works in combination with the Material and Lights workspace and will drastically change results.

You can use *any* image. There is a node called Skew that can be activated to warp the image, which may offer more desireable results for non-HDRI inputs.

Notes and preview:
![image](https://user-images.githubusercontent.com/80061436/114403865-11754180-9b9d-11eb-824c-09a944a7c36f.png)

 

## Matcap Testing (preview)

There is a workspace for previewing called 'Matcap Testing. This contains a camera setup and a model that uses different forms of shading / modelling to get an idea of what your matcap will look like when in use:

![image](https://user-images.githubusercontent.com/80061436/114403998-336ec400-9b9d-11eb-915e-fb82a6919f28.png)


You can install Matcaps into Blender as shown below. You will need to do this to test them within Blender.
![Blender Matcap Install ENG](https://user-images.githubusercontent.com/80061436/114402080-6748ea00-9b9b-11eb-8a8c-6a38a5176829.png)


## Texture Adjust

Basic workspace for adjusting / painting over a previously rendered Matcap Texture.

This workspace is still under construction and ideally will have more preset features in the future. Currently it is capable of minor manual edits to matcaps, which can still make all the difference (!) 
![image](https://user-images.githubusercontent.com/80061436/114404722-e2ab9b00-9b9d-11eb-9f81-df0786056b4b.png)
**This result can be saved and reimported follow the Matcap Testing instructions above.**
## Filtering

Compositing workspace for editing rendered Matcap Textures further. 

Contains transform properties - flip, rotate etc - as trivial as they might seem, they can drastically change output result as they effectively move the baked lighting result around by a large factor.

**This result can be saved and reimported follow the Matcap Testing instructions above.**
![image](https://user-images.githubusercontent.com/80061436/114404985-21d9ec00-9b9e-11eb-8e84-ce72fa3b3989.png)

