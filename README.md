<h1 align="center">SocialMediaEmbed&ClearURLs Bot</h1>

<p align="center">
  <a href="https://discord.com/oauth2/authorize?client_id=1505286480795406467&permissions=92224&integration_type=0&scope=bot">Click here to add the bot to your server!</a>
</p>
<br>

This bot does the exact same thing as the ClearURLs Discord bot that danieltzting made except this bot also swaps some social media website links for ones that better embed in Discord. At current, those links and the dictionary that the bot pulls from are just raw data structures in the python, but I hope to make the list configurable via slash commands. This bot also has the capability to unshorten urls. It will not attempt to unshorten urls on every link, there is also a list of urls that it will attempt to unshorten. For example: 

- youtu.be will be unshortened to youtube.com
- t.me will be unshortened to telegram.org
- bit.ly will be unshortened to whatever it links to.

I built this bot because I really hate Meta/Facebook, their horrible discord embeds and their awful login requirements and I hated remembering all of the services that would provide nice embeds in discord. So, this bot does the remembering for me!
This bot is modified from danielzting's [ClearURLs discord bot](https://github.com/danielzting/clearurls-discord-bot) as the functionality and detection of links is similar. I figured it made sense to just have one bot do all of the link manipulation instead of having multiple bots both doing link manipulation for the same thing. 
#### Disclaimer 
Public instance is running on a Proxmox node with an i5-7500. I make no guarantees of uptime.

## Permissions
The bot's permissions system is designed to be granular, minimal, and gracefully degrade in the absence of those unnecessary for basic function.

- *Read Messages* and *Send Messages* are **required** to perform the cleaning.
- *Manage Messages* is **recommended** so the bot can suppress embeds on the original message's links to reduce visual clutter. Otherwise, it will suppress embeds on its own links.
- *Read Message History* and *Add Reactions* are **optional** for the original poster to easily delete the bot's replies with the `:wastebasket:` emoji. Note that these two permissions are on by default for `@everyone`. If you want to disable react-to-remove, turn off these permissions for `@everyone` and give every human in your server a new role. This functionality also **requires** *Manage Messages* for deletion.

## Self-Hosting
It is very straightforward to host this yourself. If you do, I would love to know!

1. Download the repository with `git clone https://github.com/PapaZ810/social-media-embed--bot`
2. Get dependencies with `pip install -r requirements.txt`
3. Set up a new application at the [Discord Developer Portal](https://discord.com/developers/applications)
4. Add a bot and check the `bot` scope and the above permissions in the OAuth2 tab
5. Visit the generated link to invite the bot
6. Copy the token from the Bot tab and paste `TOKEN=[your clipboard here]` into a file named `.env`
7. Run with `python main.py`

## Terms of Service
Do unto others as you would have them do unto you.

## Privacy Policy
I collect no personal information.
