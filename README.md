# .BOT Description (version 1.1)

The .BOT description is a human-readable open-source model for building a range of conversational AI.

 Like .HTML for the web, .BOT it is a simple model that allows inexperienced developers, content authors, and engineers to build and distribute conversational user interfaces completely platform independent. **Whether they be chatbots, assistants, conversational avatars for VR or AR or even video bots the .BOT format is intended to work with a range of modalities.**

Modalities for a conversation with a bot can be the following:
- text
- voice
- facial expressions and gestures (3D avatars and video) 

This simple yet powerful approach is scalable, modular, and **integrates with a range of channels and blockchains**. It comes after many years' experience developing conversational UI, however it is also the beginning of a dialogue around how to build conversations.

Examples of channels (**bold**: already available):

- **Web** (all modalities)
- **Telegram** (text)
- **Facebook** (text)
- **Signal** (text and video)
- **Skype** (text and video avatars)
- Amazon Echo  (voice assistants)
- Snips (open-source voice assistants)
- VR (3D avatars)
- AR (3D avatars)
- Virtual Worlds (3D avatars)

## Disclaimer

These files are made available to you on an as-is and restricted basis, and may only be redistributed or sold to any third party as expressly indicated in the Terms of Use for Seed Vault.


## Objective

To define a complete bot language that gives servers the possibility to build a bot with all its logic, including external services configuration, conversation logic flow, avatar library and any other information needed to create and execute a bot.

The format used to store the .BOT description is JSON, use [this link](docs/bot_schema.json) in order to see its schema.

## Sections

The description file is divided into sections to group the parameters:

- **Basic information**: It is defined on the first level of the JSON file and includes the bot ID, name and other basic parameters.

- **Author**: It includes as much information the author wants to share about itself. It could go from anonymous bots to pretty detailed author information including address and wallet information.

- **License**: On this section is defined the license of the bot.

- **Remuneration**: Here is defined the remuneration method selected by the authors in order to collect tokens on bot usage.

- **Tags**: To help users to discover the bot into the search engine, the author is able to set different tags to the bot.

- **Modes**: Defines the modes available for the bot. Examples: chat, voice, avatar, VR.

- **Channels**: Defines the configuration of each channel where users can use the bot.

- **Media**: Here is listed all the files used to deploy the bot. It includes the thumbnail and all the files necessary to create a 3D avatar following the ACTR standard.

- **Runtime**: This section is filled by the server that is running the bot. Includes information about port, server, etc. 

- **Modules**: Defines the internal modules used on the bot.

- **Services**: Here is defined all the external services used by the bot, including main services like voice recognition, to third party services like mapping or weather information.

-- **Connections**: Bot to bot conversation configuration.

- **Logging**: Includes the information about logging method used by the bot.

- **Conversation Flow**: All the conversation logic is contained on this section. For detailed information check the [.FLOW documentation](https://github.com/SeedVault/flow).

Check the [structure documentation](docs/structure.md) in order to get more detailed information related with the sections.


## Runtime information

Even when almost all information is provided by the developer, some information is filled by the server that is running the bot. The ``runtime`` section is completed on the deployment process. 

```
    "runtime": {
      "server": "serverID",
      "type": "string",
      "IP": "ip_address",
      "port": "integer",
      "encoding": "string",
      "seedAddress": "string",
      "mode": "string",
      subscribers: "array"
    },
```

## Basic example

With a minimum number of parameters is possible to define a bot into the server:

```
"bot": {
    "ID": "",
    "name": "Example bot",
    "description": "05f079c46d096717604cc815f8eb5886",
    "version": "1.0",
    "language": "english",

    "remuneration": {
      "method": "free",
    }
    "author": {
      "name": "John Doe",
      "email": "test@example.com",
      "seedAddress": "17mmd6HfhkFB2kLy2GBbWenn48YJf7mGwg"
    },

    "modes": {
      "chat": true
    },

    "channels": {
      "channel": {
        "name": "web",
        "enabled": true,
        "mode": "chat",
       }
    },

    "media": {
      "thumbnail": "www.example.com",
    },

    "conversationFlow": {
        "url": "www.example.com/flows/flowID/32"
    }

}
```

Check a more [complete example](docs/bot_example.json) to see the structure of the other sections.

### Enhancements on version 1.1
On version 1.1 we improved the description adding:
- Sentiment Analysis server configuration
- SMTP server information
- oAuth configuration
- Extra runtime variables


## Documentation

- [Detailed information about sections](docs/structure.md)
- [.BOT description JSON schema](docs/bot_schema.json)
- [.BOT file example](docs/bot_example.json)

## Connect
Feel free to throw general questions regarding SEED and what to expect in the following months here on GitHub (or GitLab) at  @consiliera (gaby@seedtoken.io) :sunny: 

**Connect with us elsewhere** 
- [Follow us on Twitter](https://twitter.com/SEED_token)
- Always here the latest news first on [Telegram](https://t.me/seedtoken) and [Discord](https://discord.gg/Suv5bFT)

Seed Vault Code (c) Botanic Technologies, Inc. Used under license.


