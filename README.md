It’s a desktop app (Tauri, with a Rust backend and a React interface) for creating and running Minecraft Java servers from one window. These are the parts as they stand now.

Creating and running servers

You can create Vanilla, Paper, Spigot, Purpur, Fabric, Forge and NeoForge servers.
Each server can be started, stopped or restarted, and you can send it console commands.
A shutdown or restart can be scheduled on a timer, with a countdown announced in the in-game chat. Each server gets its own timer.
View Servers lists every server, and Open on any of them brings up its management screen.
The Home screen has cards that jump to the main areas. The Manage card takes you to View Servers and blinks the Open buttons.
Managing one server

You can edit server settings and server.properties.
You can set the server’s name and icon (the text and picture players see in the game’s server list), including colored text. The custom name stays saved.
The RAM setting is applied properly, including through user_jvm_args.txt for Forge and NeoForge.
You can add mods and plugins by browsing Modrinth, picking a file on your computer, or both. The right folder is chosen by server type and Minecraft version.
A runtime tab shows live memory use and tick time.
Performance tab

It shows every running server with live graphs and a running status.
Each server has an eye icon. Hovering shows who is online, and clicking opens that server’s Active Players screen.
Players and moderation

Known Players shows heads, last IP, and an approximate location from the IP.
Active Players shows who is online right now.
You can kick, ban, op and pardon players.
Bans can be timed. The manager app counts the timer itself and lifts the ban, even if the app was closed in the meantime.
Ban IP bans an address, and an IP Ban List lets you pardon addresses.
Whitelist can be turned on and off and edited from the app, with no file editing.
Operators get a red [Admin] tag in the game and a red “Admin” badge in the app.
Chat History shows only real player chat, not console lines. It flags cuss words and auto-bans racist slurs.
A moderation history is kept across all servers.
Backups

World backups are saved as zips. They can run on a per-server timer (default every 15 minutes), when a server crashes, or on demand.
Backups are kept forever by default. There’s a toggle to delete old ones after a number you choose.
Players see a chat message while a backup is running.
Stopping a server waits for a backup in progress to finish.
Known limits

I’ve never been able to compile the Rust backend here, only check its formatting and test some of the logic. You’ve been the compiler, so the first build on a new machine may show errors.
Admin tags in chat may not show on Paper, Spigot or Purpur.
A backup waits for the server to confirm it has saved the world. If that log line changes between versions, backups could be delayed.
Backups every 15 minutes with no limit can fill your disk.
