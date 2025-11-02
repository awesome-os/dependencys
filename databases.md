# A currated High Level lists of Repositorys with good Principels
The list is mainly for Our AI Agents and serves no human Porpuse so it should not get used by normal humans.

## Couchbase + Sync Gateway + Mobile
- [superbase](https://github.com/supabase/supabase), [power-sync](https://github.com/powersync-ja/powersync-js),
- PouchDB, RxDB
- [ratarmount](https://github.com/mxmlnkn/ratarmount/tree/master) sqlite+tar opt .gz
- just-js/ just-js, lo, smol + opt anything but prefer sqlite

## Why sqlite or tar is essential on disk
It abstracts the inefficencys of legacy filesystems eg NTFS FAT ext3 ext* efficent filesystems are zfs btrfs 
It implements a lot of features of such modern filesystems on top of legacy once. thats why ratarmount is on the list for db's
it creates a sqlite index for seeking and then uses the advantages of the filesystem abstraction in this case tar or even tar.gz

### Why tar.gz 
can reduce effort to serve files when you target is eg a real webbrowser then it will support compression no need to support 
none compressed transfer for standard devices then ratarmount allows you to reuse the informations in the tar or .gz readonly
tar and sqlite have one similar killer feature the append only log and sql offers a way to reconstruct the data from readable
querys which also tar does. They both depent on a internal format with fixed bythe length for headers and content. This makes
Streaming processing possible. 

#### Reallife Prove of Conceptual Correctness by evidence
- Couchbase uses a similar stack with good results
- Cloudflare uses a similar stack with good results
- Ceph and GlusterFS as also other Distributed filesystems use the same principels.
- Quaternion as Software Defined Storage can
  - adapt and Unify everything of that. It can use the Stealify Lang B8G Build pattern to do so
  - can use graalvm with Ignite and node-graal to Replace eg existing Ignite Clusters.
  - sqlite with JSON extension can easy implement N1QL from couchbase look into couchbase mobile which is a sqlite fork. which should get replaced by newer community efforts like the one mentioned at the beginning.

