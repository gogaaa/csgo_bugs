## sv\_pure bypass \#4

This exploit allows you to modify *whatever* the `.vpk` file (including the `pak01_dir.vpk`) and even `items_game.txt` (basically free skin changer).

```
bind mwheelup sv_pure_listfiles;
bind mwheeldown sv_pure_listfiles;
```

After you execute the commands above, you're pretty much done. All you need is to spam the mouse scroll wheel while connecting.

### Before you connect

You need to launch CS:GO with the modified `.vpk` files already. Normally you'd get kicked by `sv_pure` when connecting but this exploit bypasses that.

Get the `.vpk` files here: https://fromsmash.com/4fSt2~vu1T-dt

Alternatively, you can generate them by yourself. Just extract the files using [GCFScape](https://developer.valvesoftware.com/wiki/GCFScape). Then, modify them as you wish. The end step is:

```
C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive\csgo>..\bin\vpk.exe -M a pak01_dir.vpk scripts\file1.txt scripts\file2.txt
```

**Note:** I think it modifies the last `pak01_###.vpk` file AND the `pak01_dir.vpk` one. Better to compare with the orignal files to figure out what files have been modified.

### Credits

* [@szmarczak](https://github.com/szmarczak) for discovering the bug.
* [@mbhound](https://github.com/mbhound) for testing.
