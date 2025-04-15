# pvpgn_server

Dockerized PVPGN Server based on [this](https://github.com/wwmoraes/pvpgn-server-docker) project.

## Prerequisites

+ A Linux/Mac Docker cluster, which acts as a server; this server must allow traffic to 6112/4000 ports.
+ StarCraft 1.16.1 (Windows native or as [Wine](https://www.winehq.org/) based installation, whatever).

**Note:** Modern StarCraft/StarCraft Remastered or StarCraft 2 **Doesn't work**.

## Client configuration

+ Execute the `regedit` command, and go to the `HKEY_CURRENT_USER\Software\Battle.net\Configuration` key path.
+ Double click the `Battle.net gateways` key, then add the following entry at the end:

```
192.168.1.15
-5
PvPGN
```

When `192.168.1.15` is the IP address/domain name of your PvPGN server.

+ Save and close the `regedit` program.

## Running the server

To run, clone the repository and then execute:

`docker compose up`

Now the server is running and awaiting incoming connections.

## Running StarCraft

+ Open StarCraft 1.16.1 on the Windows machine.
+ Click the "Multiplayer" section, and select your favorite StarCraft version (StarCraft or StarCraft Broodwar).
+ In the "Select Connection" section, select "Battle.net".
+ Now you will see the new server (called "PvPGN"), select it and click on the "OK" button.
+ Enjoy.

No warranty, use at your own risk.
