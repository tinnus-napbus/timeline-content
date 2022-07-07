An Urbit ship's state at any time is purely a function of all events it has
previously received. These events may be key strokes, HTTP requests, Ames
packets, etc. All events are recorded in the [event
log](https://urbit.org/docs/glossary/eventlog), which is stored it the ship's
pier. In the event a ship's state snapshot gets corrupted, it can be precisely
reconstructed by replaying the event log.

A ship's event log grows progressively larger over time, as it processes more
and more events. For ordinary ships like planets, the rate of growth can be from
a few GB per year to over 20GB for more active ships, or those hosting large
groups. For Infrastructural nodes like galaxies, this can be much larger,
growing to potentially hundreds of GBs. Beyond a certain size, it's impractical
to replay event logs, as it can take an extremely long time, so the excessive
consumption of disk space is of limited value in most cases.

The solution to this is event log truncation. Events before a certain point can
be replaced by a snapshot of the state at that point. Periodically doing this
means event logs never grow very large, as the size of a ship's state usually
grows very slowly, and is currently capped at 2GB.

## More info

- [Project on Github](https://github.com/urbit/urbit/projects/1)
