# steamvr-undistort
SteamVR lens distortion adjustment utility

This is unfinished and experimental work.

Purpose is to find optimal values for the lens correction JSON file, after replacing the original frensel lenses with GearVR or other lenses.

The JSON file is read to file LH_Config_In.json via the lighthouse console at startup automatically, and coefficients are applied.
When exiting, adjusted values will be saved to LH_Config_Out.json file (not working yet). No auto update to device because it's unsafe, you can loose your original config. (Manually update after backing up original config!) 

Models are rendered three times for each color. (except center crosshair, controllers and info boxes attached to the controllers).
Switchable between solid and wireframe rendering, lens distortion correction can be toggled. (check code for keys)
Distortion correction is done inside the pixelshader. Chromatic aberration is gone with the shader code, but i think i'm missing something in the projection matrix. 
I had very limited knowledge about D3D11, matrices and transformations when starting this project. So code is unoptimized, and without comments.  


