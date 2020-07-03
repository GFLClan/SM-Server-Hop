# Server Hop
## Description
GFL's Server Hop plugin that allows players to view and connect to other game servers within GFL. This plugin also includes rotating advertisements for each servers from the list.

## Requirements
This plugin requires GFL's Core [plugin](https://github.com/GFLClan/SM-Core) and GFL's MySQL plugin to be added to the game server and enabled. Please ensure the MySQL database used for the GFL MySQL plugin has a table called `gfl_serverlist` where each server is stored.

## ConVars
* `sm_gflsh_advert_interval` => Interval in seconds to display a server advertisement to chat (default `65`).
* `sm_gflsh_gameid` => The game ID used when searching for servers within the server list. Using a value of `0` will display all servers regardless of game (default `0`).
* `sm_gflsh_locationid` => The location ID used when searching for servers within the server list. Using a value of `0` will display all servers regardless of location (default `0`).
* `sm_gflsh_refresh_interval` => How often in seconds to refresh the server list (default `500`).
* `sm_gflsh_tablename` => The table where all servers are stored in (default `"gfl_serverlist"`).
* `sm_gflsh_gametablename` => The table where all games are stored in (default `"gfl_gamelist"`).
* `sm_gflsh_advancedebug` => Whether to enable verbose logging (default `0`).
* `sm_gflsh_disableoffline` => If a server has a maxplayers count of `0`, do not advertise or show this server on the list (default `1`).
* `sm_gflsh_disablecurrent` => If enabled, the server the player is playing on will not be advertised or show on the server list (default `1`).
* `sm_gflsh_db_priority` => Database priority to use for queries executed by the plugin (default `1`).
* `sm_gflsh_db_createtable` => If enabled, the plugin will attempt to create the server and game list table automatically if it doesn't exist (default `0`).
* `sm_gflsh_new_server_announce` => If enabled, will announce any new servers on round start and rotate (default `0`).
* `sm_gflsh_use_socket` => When enabled, uses a socket to send a A2S_INFO query to the game server to collect its information instead of relying on database values (default `1`).
* `sm_gflsh_abbr` => If enabled, the server's game abbreviation will be prepended to the advertisement message (default `1`).
* `sm_gflsh_new_server_announce_method` => The method to use when displaying new servers on round start. 0 = `PrintToChatAll()`. 1 = Loop through each client and call `PrintToChat(client, "...")` (default `0`).
* `sm_gflsh_server_ip` => If the plugin fails to get the current server's IP address due to NAT-related issues or similar, you can set this CVar to represent the server IP (default `""`).

## Credits
* [Christian Deacon](https://www.linkedin.com/in/christian-deacon-902042186/) - Creator
* [GRAVE] rig0r - Socket code from one of the original Server Hop plugins released on AlliedMods.