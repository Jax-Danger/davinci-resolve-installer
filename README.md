# davinci-resolve-installer
davinci resolve installer for linux


Save the following as an `.sh` file:

```

#Linux Mint 22.x
# LEGAL NOTICE!!!!!
### EULA ####
# PLEASE NOTE.
# UPON RUNNING, USING, LOADING OR DOWNLOADING THIS BASH SCRIPT:

# YOU ARE CONSENTING TO USING THIS BASH SCRIPT AS IS AND AT YOUR OWN RISK.
# I WILL NOT BE LIABLE FOR ANY DATA LOSS YOU MAY INCUR FOR THE INCORRECT
# USAGE OR IMPLEMENTATION OR FAILURE OF TESTING ON YOUR BEHALF!
# I HAVE TESTED THIS CODE ON LINUX MINT 22 WITH DAVINCI RESOLVE 19 (FREE VERION)
# AND HAVE FOUND IT BUG FREE, AND SAFE FOR USE ON MY MACHINE.
# PLEASE BE CAREFUL AND FOLLOW THE DIRECTIONS AS GIVEN!!!



#!/bin/bash

 cd /home/$SUDO_USER/Downloads
 unzip DaVinci_Resolve_*.zip -d DaVinci_Resolve/
 chown -R $SUDO_USER:$SUDO_USER DaVinci_Resolve
 chmod 774 DaVinci_Resolve
 cd DaVinci_Resolve
 chmod +x ./DaVinci_Resolve_*.run
 SKIP_PACKAGE_CHECK=1 ./DaVinci_Resolve*.run -a
 cd /opt/resolve/libs
 mkdir not_used
 mv libgio* not_used
 mv libgmodule* not_used
 cd
 cp /usr/lib/x86_64-linux-gnu/libglib-2.0.so.0 /opt/resolve/libs/
 cd /opt/resolve/libs && sudo rm -rf libgio-2.0.so libgio-2.0.so.0 libgio-2.0.so.0.6800.4 libglib-2.0.so libglib-2.0.so.0 libglib-2.0.so.0.6800.4 libgmodule-2.0.so libgmodule-2.0.so.0 libgmodule-2.0.so.0.6800.4
 cd /home/$SUDO_USER/Downloads
 rm -rf DaVinci_Resolve


```
