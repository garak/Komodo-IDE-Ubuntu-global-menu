# Komodo-IDE-Ubuntu-global-menu
Resource to get global menu on Ubuntu

Since Komodo IDE does not support Ubuntu global menu out of the box, but there is an unofficial PPA to support it
in Komodo Edit, these instructions will allow to "port" the global menu from Komodo Edit to Komodo IDE.

**Warning**: if you are using Komodo Edit, you do not need these instructions. Just go to
[Mystic Mirage PPA](https://launchpad.net/~mystic-mirage/+archive/ubuntu/komodo-edit/+packages) and follow instructions there.

Download [komodo-edit_9.0.0+15707~unitymenubar2.tar.gz](https://launchpad.net/~mystic-mirage/+archive/ubuntu/komodo-edit/+sourcepub/4864202/+listing-archive-extra)
or any other appropriate archive, 

For your convenience, extract the ``unity-menubar`` folder somewhere in your filesystem, suppose you extract it in the ``/tmp`` folder.
Under ``unity-menubar`` folder you'll find three subfolders: ``noarch``, ``x86``, ``x86_64``. Each of these three subfolders contains a single subdolder, called ``mozilla``.

Depending on your system, you'll need to copy the content of the ``x86`` folder (if your system is 32bit) or the content of the ``x86_64`` folder (if your system is 64bit). Following instructions suppose that you're on a 64bit system, so you need to possibly adapt it in the other case.

Locate the folder in which you installed Komodo, let's suppose it's ``/opt/komodo``.

Copy ``/tmp/unity-menubar/noarch/mozilla/*`` to ``/opt/komodo/lib/mozilla/``
Copy ``/tmp/unity-menubar/x86_64/mozilla/*`` to ``/opt/komodo/lib/mozilla/``

You're done. Restart Komodo and your menu should be global.
