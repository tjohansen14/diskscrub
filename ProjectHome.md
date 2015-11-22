**scrub** overwrites hard disks, files, and other devices with repeating patterns intended to make recovering data from these devices more difficult.  Although physical destruction is unarguably the most reliable method of destroying sensitive data, it is inconvenient and costly. For certain classes of data, organizations may be willing to do the next best thing which is scribble on all the bytes until retrieval would require heroic efforts in a lab.

**scrub** implements several different algorithms for this:
  * _nnsa_ - U.S. NNSA Policy Letter NAP-14.1-C
  * _dod_ - U.S. DoD 5220.22-M
  * _usarmy_ - U.S. Army AR380-19
  * _bsi_ - German Center of Security in Information  Technologies
  * _gutmann_ - 35-pass algorithm from Peter Gutmann's [1996 paper](http://www.usenix.org/publications/library/proceedings/sec96/full_papers/gutmann/)
  * _schneier_ - algorithm described in Bruce Schneier's _Applied Cryptography_ (1996)
  * _pfitzner7_ - Roy Pfitzner's 7-random-pass method
  * _pfitzner33_ - Roy Pfitzner's 33-random-pass method

**scrub** compiles on most UNIX-like systems.
