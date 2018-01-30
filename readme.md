The Windows binaries in here are from revision fccddfe6725a1887967a279381567cc40678e888,
which was the state of the master branch on 2017-06-22. They were compiled on
VS 2015 Update 3.

The linux binaries are from revision c62fad3b19a06381ee9b82d84775698832cc4ea3, which
was the master branch from 2018-01-26. They were compiled on Ubuntu 16.04, with
clang 3.8. The binaries have been renamed for our purposes:
libEGL.so    -> libSwiftEGL.so.1
libGLESv2.so -> libSwiftGLESv2.so.2
We rename them so that we don't overwrite the system's EGL libraries.

NOTE: You should periodically rebase this repo, to get rid of old versions that are
no longer in use. Just do a `git rebase -i`, and drop the old revisions.