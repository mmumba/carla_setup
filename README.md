# carla_setup
Notes... setting up test running CARLA

Follow through setup on official CARLA website:
http://carla.readthedocs.io/en/latest/getting_started/

installation steps for version 4.18 of CARLA suggests Ubuntu 16.04. (followed through setup with Ubuntu 17.04 hope this works) Unreal Engine

Ensure you have linked github account to Unreal Engine else won't be able to pull from the UnrealGithub git repo.

When running Setup.sh in cloned CARLA repo, you may get "fatal error xlocale.h not found".
Got around this link:

```bash
     ln -s /usr/include/locale.h /usr/include/xlocale.h
```
from thread : https://answers.unrealengine.com/questions/705076/xlocaleh-not-found-on-linux.html



