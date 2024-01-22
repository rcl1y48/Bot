## 🚧 Prerequisites

- [Node.js 14+](https://nodejs.org/en/download/)
- [discord.js@14.11.0](https://www.npmjs.com/package/discord.js/v/14.11.0)
- [SQL Database]

> NOTE: SQL is needed for globalban functionality. You need to have a working SQL server to make the bot work.

## 📝 How to setup

1. To install the bots dependencies you will need to first run ``npm install`` in your terminal

> NOTE: If the bot is running on a panel host you might not need to run the install command

2. You will now need to head over to [https://discord.com/developers/applications] and create a new application, you will then need to the Bot tab and create a bot set the name and profile picture to whatever you want, then you will allow the Presence Intent, Server Members Intent and Message Content Intent. Then you will reset your bot token and paste is into the config file.

> NOTE: If you dont reset your bot token your changes wont be saved and applied and the bot wont work

> NOTE: Keep the bot token safe and do not share it

3. You will then have to edit the config.yaml file to include your SQL database info and your bot token from the discord developer portal each command is linked to a general catagory in the config which is shown below:

RoleActionPerms:
  /addrole
  /roleaddall
  /roleremove
  /rolestrip

ModerationActionPerms:
  /softban
  /kick
  /timout
  /untimeout

GlobalActionPerms:
  /globalban
  /globalunban
  /globalkick
  /globalrolestrip

> NOTE: Everyone has access to /checkban and /globalnick

You will need to update all the TicketCatagory and SupportTeam values aswell (These can all be the same but only 1 role or catagory per ticket type)

Replace the MainGuild placeholder with the guild id for your main server

UnVerifiedRole is the role id given to any user who joins
VerifiedRole is the role id given after verification is complete


4. Now you should be good to go either run ``node .`` or if you are on panel hosting set the main file to ``src/index.js``

> NOTE: If you are using panel hosting it must be either node.js or discord.js hosting or the bot wont work