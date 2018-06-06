## Sections

### Global bot information

All bots need to have a unique ID to be identified on SEED universe. Also, they need the license and pricing method to let users know the cost of that bot usage. Much information is needed in order to execute a bot correctly -e.g. language, name, etc.- that needs to be included on this section.


```
    ID": "d70f212bd5aa6739f290f64811bb45af",
    "name": "Example bot",
    "description": "This bot is an example of the capabilities of the bot",
    "version": "1.0",
    "creationDate": "2017-12-18T16:34:56.500535+00:00",
    "updateDate": "2018-05-25T19:45:11.253005+00:00",
    "language": "EN",
  ```

  The license information needs to be included on this section

```
    "license": {
      "type": "string",
      "version": "string",
      "url": "url"
    },
```

Also, The way the author wants to be remunerated when users uses the bot. There are 4 different kinds of remuneration:

- **Free**: They are free bots, not necessary to remunerate the author in order to use it.
- **Paid or by volley**: where users send tokens for each volley with the bot.
- **Subscription**: where the users send tokens to the authors in order to use the bot for a period of time.
- **Custom**: The remuneration rate is described on each volley of the bot.

```
    "remuneration": {
      "method": "string",
      "tokens": "float",
      "subscriptionDuration": "string"
    },
```
At last, on this section the author could select some tags in order to help the categorization of the bot inside the community.

```    
    "tags": [
      "weather","science","time trips"
    ],

```


### Author’s information

Some basic author information is used, including its SEED address, where the servers need to transfer the tokens collected during usage. The detail of information provided about the author depends on himself, and could be also defined as anonymous author.

```
    "author": {
      "name": "string",
      "email": "email",
      "address": "string",
      "city": "string",
      "state": "string",
      "province": "string",
      "country": "string",
      "postalCode": "string",
      "url": "string",
      "seedAddress": "string"
    },
```

### Bot Modes

It defines which modes are enabled for the bot: if it is a simple chatbot, if it includes voices or an avatar. More different methods could be included according to the new technologies that a bot could have.

```
    "modes": {
      "chat": true,
      "voice": true,
      "avatar": false,
      "realTime": false,
      "vr": false
    },
```


### Channels

Each different channel allowed by the bot needs to be defined on this section. Also, each different channel will have its own server configuration parameters and its own mode, allowing a bot to be simple chatbot on Facebook Messenger but full 3D avatar into Telegram.

So, using this section, the author will be able to select which channels its bot will be available. 

```
    "channels": {
      "channel": {
        "name": "string",
        "enabled": "boolean",
        "mode": "string",
        "server": {
          "apiKey": "string",
          "password": "string",
          "token": "string"
        }
      }
    },
```

### Media Library

All external graphical information needs to be defined on this section, including images needed to deploy a bot -e.g. the thumbnail to be published on Skype- and including the media library links or list of files needed to run a full 3D avatar according to the standard defined on ACTR.
```
    "media": {
      "thumbnail": "url",
      "avatar": {
        "library": "url",
        "prefix": "string"
      }
    },
```
Main services – TTS, Voice Recognition, Sentiment Analysis

Each main service necessary to run the bot is defined into its own section, with the service name and parameters needed.

```
"textToSpeech": {
      "provider": "string",
      "server": {
        "url": "url",
        "apiKey": "string",
        "password": "string",
        "token": "string",
        "configurationParameters": "array"
      },
      "voice": "string",
      "pitch": "string",
      "language": "string",
      "effect": "string",
      "level": "string"
    },
```

### Other services

All other services used by a bot to expand its functionality -e.g. mapping, exchange, weather, etc.- are defined on this section, including server configuration and any extra parameter needed in order to interact with those services.

```
    "services": {
      "provider": {
        "name": "string",
        "status": "boolean",
        "url": "www.example.com/",
        "configurationParameters": "array"
      }
    }
```

### Logging

On the bot definition file it is included the type of logging used by the bot and according to the server and channel restrictions.

```
    "logging": {
      "enabled": true,
      "method": "plain",
      "server": "https://www.example.com/logging/"
    },
```


### Conversation Flow

All the conversation flows are included on this section as simple URL pointing to the flows or including the full content of the conversation flow itself into this section.

The conversation flow includes all logic enabled on SEED environment, including volleys, forms, user cards and any type of nodes enabled on any conversation.

One or more conversation flows are allowed by bot.


## Next Steps



## Disclaimer

These files are made available to you on an as-is and restricted basis, and may only be redistributed or sold to any third party as expressly indicated in the Terms of Use for Seed Vault.

Seed Vault Code (c) Botanic Technologies, Inc. Used under license.