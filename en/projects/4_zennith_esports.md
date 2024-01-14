![Zennith Esports](/img/zennithesports.jpeg)

### Gaming Engineering and Automation

* * *

I’ve been always fan of motorsports and simulation, but this got into the next level with Zennith Esports, a Spanish based simracing team. With them, I started to develop a series of automations and tools to achive some pretty cool things.

*   Made with **Golang**
*   Event automations and broadcasting mode
*   Python Client with real time data emitting on event start (you can see the live timing aside the broadcast coming directly from the drivers clients)
*   Live telementry and strategy analyzer
*   Comunity manager/Twitter event announces automations
*   PHP/MongoDB Backend, synced with Nexcloud auth and calendars
*   Setup sharing automations

![Crypto logo](/img/streaming.jpeg)

### Nobody at the wheel

* * *

The system emits real-time data broadcasting (through a Python client running in the computer of each team member which detects the execution of the sim and check events and participations against a PHP API).

All is automated:

*   New section comes from Twitter API requests from tweets with an specific hashtag
*   User profiles are updated syncing with the sim APIs grabbing all the drivers stats, Events are completely automated (system gets in Live mode with all the events data and live broadcast (twitch or youtube) with the real time feed by the clients).
*   The community manager is also a bot, the system generates a PNG with the announce of the events, and the system tweets it the target day by morning and with the event start

![Crypto logo](/img/strategist.jpeg)

### Sources are private

* * *

I'm sorry, but **this is a personal private project**, so the sources are not available publicly. Anyway, the code could be reviewed under request.
