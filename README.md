# xbps-mini-builder

This is the XBPS mini builder, use it when you want to create a mirror
containing restricted packages that the Void project doesn't build for
you.  Put this script in a directory on its own and put a
`packages.list` next to it that contians the packages you want to
build.  You can also add an `xbps-src.conf` to be used during builds.

Run the script on a cron or with `snooze(1)` once a day to get
updates, all other tasks are handled for you!
