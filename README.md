patch-hook
==============

add-hook takes a package name as an argument and creates a hook in /etc/pacman.d/hooks which will run patch-hook for that package

patch-hook can be run manually on a package which is passed as an argument.
Or it can be called from a hook.
Configuration is via '/etc/patch-hook.conf', '/etc/patch-hook/patch-hook.conf', '/etc/patch-hook/{pkg_to_patch}.conf' (Least precidence first listed)

patch-hook.conf.example shows available options.

By default directories are created under /var/patch-hook.  
By default patch-hook will look for patches in dir /var/patch-hook/patches/{pkg_to_patch}  
Anything .diff or .patch in that dir will be applied as a patch. (except dummy.diff)  
A file can also be placed in /var/patch-hook/patches/{pkg_to_patch} called {pkg_to_patch}.py  
This file can contain addtional python code which can be run at various points in the script.  Useful for ediiting PKGBUILD's.

A work in progress. I might accidentally introduce a bug which deletes your root partition. The bug might already be there ?
If that's unacceptable **DON'T USE IT**.

patch_hook_path = '/usr/local/bin/patch-hook'   
patch-hook needs to be there or change the line above in add-hook to reflect where it is located.
