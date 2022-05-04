Inspired by: [Sleepingpirates/Invitarr](https://github.com/Sleepingpirates/Invitarr)
<br>
Invitarr is a discord bot that automates and manages inviting users in a Discord server to a Plex server.
## Features
Invitarr can:
 - Monitor a role in a Discord server to serve Plex invites to users who get the role
 - Store users' invite information in a local database
 - More coming soon!
## Installation & Usage
Once Invitarr reaches a good featureset, it will be released to easily pull into docker. For now, you can manually run the app using the steps below:
<br>
1. Create a bot on the [Discord Applications page](https://discord.com/developers/applications)
2. Make sure your bot has access to the `GUILD_MEMBERS` intent
3. Clone the repository
```
git clone https://github.com/Jellayy/Invitarr.git
```
4. Configure the `config.ini` file
```
[Discord]
command prefix = .
bot token = YOUR_BOT_TOKEN

[Plex]
email = YOUR_EMAIL_OR_USER
password = YOUR_PASSWORD
server = YOUR_SERVER_NAME

[Role Monitoring]
enable = 1
monitored role = YOUR_ROLE_NAME
```
5. Install dependencies
```
pip install -r requirements.txt
```
6. Run
```
python bot.py
```
Assuming you have configured everything correctly, Invitarr will send DM invites to any user that recieves the configures monitored role. Make sure your users have their DMs open!
## Commands
`.get_db` Sends a txt copy of the user DB to discord. This contains users' Plex emails. If your users don't want these publicly shared, restrict the bot's access to public channels.
