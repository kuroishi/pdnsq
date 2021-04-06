pdnsq
======
Parallel DNS Query command

Ready for use
--------------
```
% carton install --deployment
:
Successfully installed Canary-Stability-2013
Successfully installed AnyEvent-7.17
2 distributions installed
:
```

Usage
-----
```
% carton exec -- ./pdnsq  www.yahoo.co.jp
querying to 9.9.9.9
querying to 1.1.1.1
querying to 8.8.8.8
ret: 183.79.219.252 from 1.1.1.1 (0.049725[sec])
```

```
% carton exec -- ./pdnsq -d -s 1.1.1.1 1.0.0.1 9.9.9.9 -- www.yahoo.co.jp
querying to 1.1.1.1
querying to 9.9.9.9
querying to 1.0.0.1
ret: 183.79.219.252 from 1.1.1.1 (0.033463[sec])
ret: 183.79.219.252 from 1.0.0.1 (0.033407[sec])
ret: 183.79.219.252 from 9.9.9.9 (0.275080[sec])
```
