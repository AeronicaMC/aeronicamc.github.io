---
title: "How to Update mxTune-1.16.5-beta worlds to rc.1"
date: 2024-01-05T10:53:34-06:00
categories:
  - mxtune
tags:
  - how-to
  - update
  - "1.16.5"
classes: wide
---

#### How to update a save/world from ``mxtune-1.16.5-2.0.0-beta-2023-12-08.76721460`` to ``mxtune-1.16.5-3.0.0-rc-1``

If you are not upgrading a world and just starting a new world then you can ignore this post.
{: .notice--primary}

  1) Before upgrading ensure your worldsave is using ``mxtune-1.16.5-2.0.0-beta-2023-12-08.76721460``. 

  2) Close the game or stop the server. Locate the mxtune server config, example:
  "``C:\MyMCStuff\SomeModPack\saves\SomeWorld\serverconfig\mxtune-server.toml``" 

  3) Edit the mxtune-server.toml and set ``sheetMusicLifeInDays = 99999`` 

{% include figure image_path="/assets/images/mxtune-server-conf-pre-dump.png"%}

  5) Start the client and/or server as appropriate and enter the world. 

  6) With owner/op rights excute the comand ``/mxtune music dump``. This can also be done from the server terminal/console: ``mxtune music
dump``

{% include figure image_path="/assets/images/mxtune-dump-execute.png"%}

  7) The number of records will be displayed/logged. The number depends on how may pieces of Sheet Music were created for all players. 

  8) Stop the game/server. 

{% include figure image_path="/assets/images/mxtune-dump-result.png"%}

  9) Replace the mxtune jar with the new version mxtune-1.16.5-3.0.0-rc-1. 

  10) Start the game/server and review the mxtune-server.toml. Confirm ``sheetMusicExpires = false`` 

{% include figure image_path="/assets/images/mxtune-server-conf-pre-convert.png"%}

  11) With op rights execute the command ``/mxtune music convert``. This can also be done from the server terminal/console: ``mxtune music
convert``. 

{% include figure image_path="/assets/images/mxtune-convert-execute.png"%}

  12) Number of files written will be displayed/logged. The number depends on how may pieces of Sheet Music were created for all players. 

{% include figure image_path="/assets/images/mxtune-convert-result.png"%}

**Note:**    
  The images used were taken from different test saves and the number of records dumped and converted to files don't
match. In practice these should match.
{: .notice--primary}
