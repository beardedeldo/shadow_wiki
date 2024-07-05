# Arma Reforger Server Setup Guide

## SteamCMD Setup

**Note: This tutorial has been tested on Ubuntu.**

### 1. Install SteamCMD

Visit the [SteamCMD documentation](https://developer.valvesoftware.com/wiki/SteamCMD) for the latest instructions.

- Download SteamCMD.
- Start the SteamCMD client: `steamcmd`
  - *Once started, you can set a custom installation path using the `force_install_dir` command:* `force_install_dir /path/to/installation`
  - Log in as anonymous: `login anonymous`

**Note:** If you skip the `force_install_dir` step, SteamCMD will install by default in `/home/<username>/steam/steamapps/common`.

### 2. Download and Install Arma Reforger Server

Run the following commands in SteamCMD:

```bash
app_update 1874900
quit
```

### 3. Test Arma Reforger Server

Navigate to the installation directory and test the Arma Reforger Server:

```bash
./ArmaReforgerServer
```

### 4. Create a Custom Server Config

- Navigate to the Arma Reforger Server directory:

```bash
cd /home/bearded/Steam/steamapps/common/Arma\ Reforger\ Server
```

- Create a new directory called "Configs":

```bash
mkdir Configs
```

- Change directory to "Configs" and create a `server.json` file:

```bash
cd Configs
nano server.json  # Use your preferred text editor
```

Example `server.json` file:

```json
{
	"bindAddress": "0.0.0.0",
	"bindPort": 2001,
	"publicAddress": "Look up your static IP",
	"publicPort": 2001,
	"a2s": {
		"address": "Look up your static IP",
		"port": 17777
	},
	"game": {
		"name": "SERVER_NAME",
		"password": "STRING",
		"passwordAdmin": "STRING",
		"admins" : [
			"TYPE_YOUR_STEAM_ID"
		],
		"scenarioId": "{ECC61978EDCC2B5A}Missions/23_Campaign.conf",
		"maxPlayers": 32,
		"visible": true,
		"crossPlatform": true,
		"supportedPlatforms": [
			"PLATFORM_PC",
			"PLATFORM_XBL"
		],
		"gameProperties": {
			"serverMaxViewDistance": 2500,
			"serverMinGrassDistance": 50,
			"networkViewDistance": 1000,
			"disableThirdPerson": true,
			"fastValidation": true,
			"battlEye": true,
			"VONDisableUI": true,
			"VONDisableDirectSpeechUI": true,
			"missionHeader": {
				"m_iPlayerCount": 40,
				"m_eEditableGameFlags": 6,
				"m_eDefaultGameFlags": 6,
				"other": "values"
			}
		},
		"mods": [
		]
	},
	"operating": {
		"lobbyPlayerSynchronise": true
	}
}
```

Save and exit the text editor. Adjust the configuration based on your preferences and requirements.

### 5. Enable Port Forwarding

- Ensure that the following ports are forwarded to your server machine:

    **ARMA Reforger - Steam:**
    - TCP: 27015, 27036
    - UDP: 2001, 17777, 27015, 27031-27036

    **ARMA Reforger - Xbox Series X:**
    - TCP: 3074
    - UDP: 88, 500, 3074, 3544, 4500

Adjust your router settings to forward these ports. Set both the internal and external ports to 2001 for TCP and UDP.

This completes the setup of the ARMA Reforger Server, including custom configuration and port forwarding. Adjust the instructions based on your specific router interface.


