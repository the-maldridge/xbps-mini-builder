# xbps-mini-builder

This is the XBPS mini builder, use it when you want to create a mirror
containing restricted packages that the Void project doesn't build for you. Put
this script in a directory on its own and put a `packages.list` next to it that
contains the packages you want to build. You can also add an `xbps-src.conf` to
be used during builds.

Run the script on a cron or with `snooze(1)` once a day to get updates, all
other tasks are handled for you!

## Notes

- Create `packages.list` and `xbps-src.conf` before running `xbps-mini-builder`
- Run the script *only* as the user you plan to run it as normally, or the
   repository will have broken permissions.
- To build restricted packages, you must add `XBPS_ALLOW_RESTRICTED=yes` to
   `xbps-src.conf`

## Troubleshooting

If you do add packages to `packages.list` after the script has initialized the
repository, or forgot to enable the building of restricted packages, the script
will not build the package files until they are updated upstream. To manually
build a specific package, run `./xbps-mini-builder <package>` and it will build
the package, whether it has changed or not. Remember to only run this as the
user that will be running the script normally.
