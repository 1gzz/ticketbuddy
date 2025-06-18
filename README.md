# TicketBuddy <img src="https://i.imgur.com/Vo48F9E.png" alt="TicketBot Logo" width="20" />

TicketBuddy is a public Discord bot designed to help you manage support tickets in your server. This bot is easy to use and does not require access to the source code because you can invite it to your server & use it.

## Features
- Create and manage support tickets with categories
- Ticket panel with customizable buttons
- Ticket transcripts (sent to a channel & user DMs)
- Logging of ticket events
- Staff and Ticket Blacklist roles
- Easy setup with slash commands
- User-friendly and fast

## How to Invite TicketBuddy

1. **Invite Link**
   - [Click here to invite TicketBuddy to your server](https://discord.com/oauth2/authorize?client_id=1384684790250344499)

2. **Permissions**
   - Grant the bot permissions to manage channels, roles, send messages, and read message history.

## Setup Guide

1. **Set Ticket Categories**
   - `/setticketcategories categories:<emoji:name, emoji:name, ...>`
   - Example: `/setticketcategories categories:🌐:Support, 🛠️:Tech, Billing`
2. **Set Parent Category for Tickets**
   - `/setticketcategory category:<category channel>`
3. **Set Staff Role**
   - `/setstaffrole role:<role>`
4. **Set Ticket Blacklist Role (users with this role cannot create tickets)**
   - `/setblacklistrole role:<role>`
5. **Set Transcript Channel**
   - `/settranscriptchannel channel:<channel>`
6. **Set Logs Channel**
   - `/setlogschannel channel:<channel>`
7. **Set Ticket Panel Channel**
   - `/setticketpanelchannel channel:<channel>`
8. **Send the Ticket Panel**
   - `/sendticketpanel`
9. **Enable/Disable Transcripts to User DMs**
   - `/settranscriptdm enabled:true|false`
10. **View Current Settings**
    - `/viewsettings`

## User Commands

- **Open a Ticket:** Click a button in the ticket panel
- **Bot Info:** `/info` — Bot and support info

## Example Workflow
1. Admin sets up categories, staff role, and panel channel using the commands above.
2. Admin sends the ticket panel to a channel.
3. Users click a button to open a ticket. A private channel is created for them and staff.
4. Staff and user chat in the ticket channel. Staff can close the ticket with the `Close` button.
5. When closed, a transcript is sent to the transcript channel and optionally to the user’s DMs.

## Support
If you need help or have questions, please contact the bot owner or join the [support server](https://discord.gg/NbaeDx8kDN).

---

*TicketBuddy is not open source. You cannot self-host or modify the bot's code. Please use the official invite link above to add it to your server.*