# carla_setup
Notes... setting up test running CARLA

Follow through setup on official CARLA website:
http://carla.readthedocs.io/en/latest/getting_started/

Installation steps for version 4.18 of CARLA suggests Ubuntu 16.04. (followed through setup with Ubuntu 17.04 hope this works) Unreal Engine. Built CARLA and Unreal Engine following build instructions on webpage:

https://carla.readthedocs.io/en/latest/how_to_build_on_linux/


Ensure you have linked github account to Unreal Engine else won't be able to pull from the UnrealGithub git repo.

When running Setup.sh in cloned CARLA repo, you may get "fatal error xlocale.h not found".
Got around this link:

```bash
     ln -s /usr/include/locale.h /usr/include/xlocale.h
```
from thread : https://answers.unrealengine.com/questions/705076/xlocaleh-not-found-on-linux.html

When running build for CARLA instead of single line suggested before declaring/exporting variable UE4_ROOT, broke this out into two steps:
```bash
   export UE4_ROOT=<path to UnrealEngine>/UnrealEngine_4.18
   
```

Launching UR4 with CARLA suggested
```bash
  $ cd Unreal/CarlaUE4
  $ ~/UnrealEngine_4.18/Engine/Binaries/Linux/UE4Editor "$PWD/CarlaUE4.uproject"
```
  Second launch didn't work but launching UE4 without passing it the CarlaUE4.uproject first
  
  ```bash
      $ ~/UnrealEngine_4.18/Engine/Binaries/Linux/UE4Editor 
   ```
   then attempting to open CarlaUE4.uproject once UE4 launches.
   attempt at launching copy of CarlaUE4.uproject resultded in Segmentation fault
   
  Changing directory to "CarlaUE4 4.18/" and running copy of CarlaUE4.uproject Town01 seems to work. (one of two town layouts as of this writing).
  
  ```bash 
     cd Unreal/CarlaUE4 4.18
     $ ~/UnrealEngine_4.18/Engine/Binaries/Linux/UE4Editor 
  ```
 Can also launch Carla in stand alone mode, download compiled version here:
 https://github.com/carla-simulator/carla/releases/tag/0.8.3
 
 unzip and run script
 ```bash
    ./carlaUE4.sh
 ```
 
 fills whole screen so better to launch as windowed 
 ```bash
     ./CarlaUE4.sh -windowed /Game/Maps/Town02 
 ```
 
 Can quickly connect a client by running above standalone Carla script and launching a client
 by following through
 https://carla.readthedocs.io/en/latest/connecting_the_client/
 
 
  
  
  Interesting: https://ai.intel.com/reinforcement-learning-coach-carla-qr-dqn/
  
  
 
    
