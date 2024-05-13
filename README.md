patch-hook
==============

add-hook takes a package name as an argument and creates a hook in /etc/pacman.d/hooks which will run patch-hook for that package

patch-hook can be run manually on a package which is passed as an argument.
Or it can be called from a hook.
Configuration is via '/etc/patch-hook.conf', '/etc/patch-hook/patch-hook.conf', '/etc/patch-hook/{pkg_to_patch}.conf' (Least precidence first listed)

patch-hook.conf.example shows available options.

By default directories are created under /var/patch-hook.

A work in progress. I might accidentally introduce a bug which deletes your root partition. The bug might already be there ?
If that's unacceptable **DON'T USE IT**.
