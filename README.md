# TicketBuddy <img src="https://i.imgur.com/Vo48F9E.png" alt="TicketBot Logo" width="20" />

TicketBuddy is a public Discord bot designed to help you manage support tickets in your server. This bot is easy to use and does not require access to the source code because you can invite it to your server & use it.

## Features
- 🎫 Create and manage support tickets with customizable categories
- 🎛️ Interactive ticket panel with up to 5 customizable buttons
- 📄 Automatic ticket transcripts (sent to channels & user DMs)
- 📊 Comprehensive logging of all ticket events
- 👥 Staff role management and ticket blacklist system
- ⚡ Easy setup with intelligent slash commands
- 🛡️ Advanced error handling and automatic recovery (so no downtime)
- ✅ Smart channel type validation to prevent configuration errors
- 🚀 User-friendly, fast, and production-ready

## How to Invite TicketBuddy

1. **Invite Link**
   - [Click here to invite TicketBuddy to your server](https://discord.com/oauth2/authorize?client_id=1384684790250344499)

   - Or here if that didn't work: https://discord.com/oauth2/authorize?client_id=1384684790250344499

2. **Permissions**
   - Grant the bot permissions to manage channels, roles, send messages, and read message history.

## Setup Guide

1. **Set Ticket Categories** *(Required)*
   - `/setticketbuttons categories:<name, name, ...>`
   - Example: `/setticketbuttons categories: Support, Billing, Other`
   - ⚠️ Maximum of 5 categories allowed (Discord button limit)

2. **Set Parent Category for Tickets** *(Required)*
   - `/setticketcategory category:<category channel>`
   - 📁 Must select a **category channel** (not text/voice)
   - This is where all ticket channels will be organized

3. **Set Staff Role** *(Required)*
   - `/setstaffrole role:<role>`
   - Staff members can close tickets and are automatically pinged

4. **Set Ticket Panel Channel** *(Required)*
   - `/setticketpanelchannel channel:<text channel>`
   - 💬 Must select a **text channel** (not category/voice)
   - This is where users will see and interact with the ticket buttons

5. **Set Transcript Channel** *(Required)*
   - `/settranscriptchannel channel:<text channel>`
   - 💬 Must select a **text channel** (not category/voice)
   - Ticket transcripts will be automatically saved here

6. **Set Logs Channel** *(Required)*
   - `/setlogschannel channel:<text channel>`
   - 💬 Must select a **text channel** (not category/voice)
   - All ticket events will be logged here

7. **Set Ticket Blacklist Role** *(Required)*
   - `/setblacklistrole role:<role>`
   - Users with this role cannot create tickets

8. **Send the Ticket Panel** *(Final Step)*
   - `/sendticketpanel`
   - Creates the interactive button panel in your configured channel

9. **Configure Transcript DMs** *(Optional)*
   - `/settranscriptdm enabled:true|false`
   - Enable/disable sending transcripts to users via DM (default on disabled)

10. **View Current Settings**
    - `/viewsettings`
    - Review all your current bot configuration

## User Commands

- **Open a Ticket:** Click a button in the ticket panel
- **Bot Info:** `/info` — Bot and support information
- **Help:** `/help` — Complete command list
- **How to Use:** `/howtouse` — Step-by-step setup guide
- **Statistics:** `/stats` — Bot performance and server statistics

## Advanced Features

### 🛡️ **Error Handling & Reliability**
- Comprehensive error catching and reporting
- Graceful recovery from database corruption
- Smart retry mechanisms for failed operations

### 🔄 **Live Database Reloading**
- Automatic detection of database file changes
- No bot restarts required for configuration updates
- Debounced reloading to prevent performance issues
- Race condition protection with database locks

### ✅ **Smart Validation**
- Channel type validation prevents configuration errors
- Input sanitization for all user-provided data
- Automatic cleanup of expired cooldowns and stale data
- Discord API limit compliance (5 buttons max per panel)

### 📊 **Comprehensive Logging**
- Detailed ticket creation and closure logs
- User action tracking with timestamps
- Error context preservation for debugging

## Example Workflow
1. Admin sets up buttons, staff role, and other stuff using the commands above.
2. Admin sends the ticket panel to a channel using /sendticketpanel.
3. Users click a button to open a ticket. A private channel is created for them and staff.
4. Staff and user chat in the ticket channel. Staff can close the ticket with the `Close` button.
5. When closed, a transcript is sent to the transcript channel and optionally to the user’s DMs.

## Support
If you need help or have questions, please contact the bot owner or join the [support server](https://discord.gg/NbaeDx8kDN).

---

*TicketBuddy is not open source. You cannot self-host or modify the bot's code. Please use the official invite link above to add it to your server.*
