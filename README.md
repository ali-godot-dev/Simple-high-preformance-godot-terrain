# Simple-high-preformance-godot-terrain
This is a terrain system made in Godot 4.7.2 stable

It uses 3 heightmap textures sampled with world position at different scales it's a good idea to use it in the following "MAD" architecture 

First heightmap should be the Main heightmap I recommend the main heightmap to be a high quality heightmap from real terrain or software like gaea, don't worry about infinite terrain yet 
The 2nd heightmap should be the Adjustments heightmap , this one is important for infinite terrain and to use it you can just add a NoiseTexture2D to it, this makes tiling the heightmap without obvious repetition easier you can mix it with a gradient texture to tune the areas it influences 
The 3rd heightmap is the Details heightmap you can use it to add small details though it would only be viable if your terrain has higher subdivisions 
Each heightmap can be tuned , the details heightmap for example uses power to scale
