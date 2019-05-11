# Discord Audit Log Bot

A Discord bot that fills in the gaps in Discord's Audit Log.

This bot logs: message edits and deletions, username changes, when a member joins, changes, or leaves voice, and when a member joins or leaves the server.

<div align="center">
  <img src="https://raw.githubusercontent.com/peterthehan/discord-audit-log-bot/master/assets/messageEdit.png" />
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/peterthehan/discord-audit-log-bot/master/assets/messageDelete.png" />
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/peterthehan/discord-audit-log-bot/master/assets/usernameChange.png" />
</div>

<div align="center">
  <img src="https://raw.githubusercontent.com/peterthehan/discord-audit-log-bot/master/assets/memberLeave.png" />
</div>

## Setup

1. Adapt and follow the steps found in [create-discord-bot](https://github.com/peterthehan/create-discord-bot).

2. Open [src/config.js](https://github.com/peterthehan/discord-audit-log-bot/blob/master/src/config.js) to configure your own settings:

```js
addColor: 3066993,
editColor: 15105570,
deleteColor: 15277667,
deleteTimeThreshold: 1,
guildChannelMap: {
  'GUILD_1_ID': 'TEXT_CHANNEL_1_ID',
  'GUILD_2_ID': 'TEXT_CHANNEL_2_ID',
  'GUILD_3_ID': 'TEXT_CHANNEL_3_ID',
  // ...Add as many guild-channel mappings as you want.
}
```

> Message deletions that occur in less time than the `deleteTimeThreshold` (in seconds) will not be logged.
