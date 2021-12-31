# aosp-enable-polly
These are clang wrappers to enable polly when building rom.
Android 11 and upper contains polly support in their clang direcotry, however it requires manually load.

First rename(or copy) clang and clang++ to add ".r" suffix

And then create links "clang.r.real" "clang++.r.real" to the real clang excutable.

Script checks if we are building assemble file and disable the plugin because Polly won't load correctly on this case. 

