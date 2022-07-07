Scries are read-only requests for data from Arvo, Urbit's operating system. So
far, scries have been limited to the local ship. Content distribution, also
known as remote scries, extends Arvo's scry system across the network.

Remote scries improve performance when fetching content over the network and
reduce event log bloat. Initially they'll be limited to Clay (the filesystem
vane), but eventually they'll be integrated into Gall for use in userspace.
Remote scries lay the groundwork for eventual parallel processing of such
network requests, and also a reform of Gall subscription mechanics.

## More info

- [Pull request on Github](https://github.com/urbit/urbit/pull/5878)
