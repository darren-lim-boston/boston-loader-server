# Boston Minecraft Server

Welcome to the Boston Minecraft server. Here, you can find information about running the server on your computer and some more detailed information about what is included in the server.

![Boston Commons in Minecraft](images/boston-commons-example.jpg?raw=true)

![Hurricane Preview](images/hurricane-preview.jpg?raw=true)

![Hurricane](images/hurricane.gif?raw=true)

## See the game in action!

[Developer's Playthrough](https://www.youtube.com/watch?v=mvZx6Q6UUJM&feature=youtu.be)

- Notes: the core games are included in this repository as-is, but some smaller aspects may have changed to adjust for bugs/narration purposes.

# How do I...

## ...play the game?

You can play the Boston Minecraft server in a few steps. The below steps assume that the player is not too familiar with server setup. **Additionally, the game is currently configured to run on 1.18.2. There are no guarantees that newer versions will work seamlessly.**

1) Make sure you have Java 17 installed (you can find the JDK [here](https://adoptium.net/))

2) Run the server!

- *If you are on a Windows computer*, you want to run the server using the `RUN.bat` file. If this file does not work, edit the file and specify where your `java` is located from the Java you should have installed in Step 1, changing the file respectively.

- *If you are on a Linux/Mac computer,* you should be able to run the server using the `start.sh` file. Again, make sure the `java` points to the correct location for Java 17.

3) You can log onto the server on your local machine by connecting to `localhost`. If you are trying to connect from a different computer on the same wireless network, you can connect by finding your local IP address and connecting via this local IP address. If you are trying to connect from a different network, then you will need to port forward the server on port 25565.

4) To start the game, simply call the `/game easy` command. Some examples of what you can play are below:

- If you want to play on normal difficulty (less time), then run:

        /game normal

- If you want to play a particular game, then you can run:

        /game <flood/heatwave/hurricane> <easy/normal> <name>

- For instance, to play the hurricane game on normal difficulty as Steve, run:

        /game hurricane normal Steve

Notes:

- only players who are on the server when the game starts will be included in the game

- you cannot stop a game once it has started

## ...update the game to a newer version?

NOTE: in order to update the game, you will most likely need to have Java/Minecraft development experience.

If you want to update the game to a newer version, you may have to get your hands dirty and modify and build the plugins themselves, located [here](https://github.com/darren-lim-boston/boston-loader-plugins). You will also have to update the Citizens plugin to the same version as your Minecraft version, found by looking [here](https://ci.citizensnpcs.co/job/citizens2/). Finally, you may have to update worldedit, found [here](https://dev.bukkit.org/projects/worldedit/files).

To update the server itself, you will have to download a new `paper.jar` corresponding to the version of Minecraft you wish to play. Look [here](https://papermc.io/downloads) for the downloads, and make sure to name the file `paper.jar`.

Finally, you may have to edit the BostonSimulations.jar and BostonLoader.jar plugins if they are no longer working in the new version. Again, you can find them [here](https://github.com/darren-lim-boston/boston-loader-plugins). You may need to recompile the plugin in a newer dependency version, and ensure that no breaking changes were made. 

## ...make my own games/worlds using BostonSimulations?

NOTE: making your own games requires you being familiar with Java. Making your own worlds may require you to be familiar with scripting.

Look at the [boston-loader-plugins](https://github.com/darren-lim-boston/boston-loader-plugins) repository, specifically under `boston-simulations`, to start figuring out how to make your own games within this platform.

To make your own worlds, start by looking at the [boston-loader-convert](https://github.com/darren-lim-boston/boston-loader-convert) repository.

# What's included?

## Worlds

There are a few world folders, 2 of which are important for the game to run:

`world-game`: main world where the game will take place

`world-city`: world that has the entirety of the City of Boston

`world-backup`: backup of the world-game. this world file is used when the game starts to reset the world!

The rest of the worlds in the folder are not as important.

`world-test`: testing world. ignore

`world`: testing world, ignore

## Plugins

The server includes various plugins. **Only `BostonSimulations.jar` and `Citizens-2.0.29-b2542.jar` are required to play the game.**

The `BostonSimulations.jar` file holds the game logic, and allows you to start the game.

The `Citizens-2.0.29-b2542.jar` file is a plugin that allows you to view NPCs in-game.

`BostonLoader.jar` is used to load the schematics into the game. See the [boston-loader-convert](https://github.com/darren-lim-boston/boston-loader-convert) repository for more information (advanced).

The rest of the plugins: `AutoPluginReload.jar`, `PlugMan.jar`, and `worldedit-bukkit-7.2.10.jar` are helper plugins used to build out the world and support development.

## Some notable locations in world-city (X Y Z)

If you are op, you can teleport to these locations and check them out! Use `/simulation world world-city` to teleport to this world, then `tp X Y Z` to teleport to these locations.

*franklin park zoo*: 3745 27 -3388

*fenway park*: 3466 13 -4961

*esplanade*: 3935 25 -5304