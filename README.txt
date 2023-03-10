This implementation was made in Unreal engine version 5.0.3, 
and should only require the engine to run, with no extra features needed.

If the map with pre-made water and floating objects blueprints is not loaded when 
opening the project, open the 'ThirdPersonMap' in Content/ThirdPerson/Maps



Swimming -
To set up swimming, the swimming water blueprint will need to be configured to the area and
depth of water you want to character to be able to swim in, using the water surface for the 
area, and the Water Depth box component for the depth. The Swimming Depth plane should be
placed at the depth within the water where you want the player to start swimming. The player 
will only stop swimming when the exit the water entirely, meaning when they stop overlapping
any and all of its components. 


Buoyancy - 
To make a buoyant object, create an instance of the 'Floating Object' parameter. You can change 
the mesh component to any mesh you like, so long as it has collision. 
Create as many float points as needed using the 'Number of Float Points' parameter. This is
the exact amount, meaning setting it to '1' will create 1 float point.
Set the positions of these float points using the position array below, ideally one in each
corner. 

Consider the mass of your object, set within the object's Physics component, and the 
floating power of any water you want it to float in, set with the water's parameter, both of
which will affect how much or little the object floats.
Then, when the object is in water, if its mass is less than the water's floating power and wave
height, it will float. No more set-up needed.


Materials -
To test the surface material opacity mask, three example masks have been provided. 
You can find these within Content/Water/Assets/Materials/Textures/Masks,
or search for 'ExampleMask'. 



Credits -
Splash sound effect from the BBC Sound Effect Archive -
Available at: https://sound-effects.bbcrewind.co.uk/search?durations=0-9&q=water&resultSize=20

Caustics texture from Abode Substance 3D Designer examples -
Available at: https://substance3d.adobe.com/documentation/sddoc/version-11-2-215286709.html

Other textures avaliable from Ben Cloward youtube - specfically water material tutorials -
Available at: https://www.youtube.com/@BenCloward