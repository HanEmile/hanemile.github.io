# semiautohack

Now i just thought about the concept of auto hacking again and had some Idea I thought would be great written down, so here it is

:::toc

## intro

Normally, when thinking of "auto hacking", the main focus lies on automatically hacking (hence the name), without any further user input. Throw a url in, get some juicy findings out.

Now this is quite nice, but not perfect, as you also might have realized that auto hacking is hard. Very hard. Now we've still got the opposite with "manual hacking". Manual hacking consists of making requests yourself, looking into binaries yourself, although most of these tasks are supported by tools which can be seen as a way to automatically do stuff (for example format some kind of HTTP request or disassemble a binary into something you can read).

Now in the case of manual hacking, you tell the computer what you want to do and what to look into. The programs you use can give you some hints on what might be interesting or so, but the program (at least most of them) won't tell you to look into something more specific.

## the idea itself

Now the idea is to give computers more power. This is done by letting them work together, passing "jobs", "requests" and information between them.

I've got some idea on how the end result might look like, I'll describe it here. There isn't anything related to the internals figured out at this point, this might change in the future.

So in the end, I'm imagining a system in which we can pass some kind of worker A for example a url and the worker A will start to take it apart. The worker A might "know" (concept introduced later) some other worker B that might "know" how to handle it, so worker A passes the information to worker B. Worker B could for example start spidering the url and handle the results by passing them to some kind of "auditor" (which itself is another worker). The auditor then audits the results and passes them on.

### information passing

Now I've often mentioned "passes the information on" or so. The whole implementation might just work using the ActivityPub protocol (inboxes/outboxes/...). Now don't panic, I'm not sure myself if this might even work, but I'm going to give it a try. If this does turn out to work out, the whole system might get quite intersting, as we could use bots and people interchangeablt. Say some bot finds something interesting, it could pass it to another bot or to some other human which then looks into it further.

I'm quite intrigued building such a system, as this is something I haven't seen before (and I do understand that it isn't as simple as it might seem at first glance).

## bots

Now the bot's might be one of the interesting concepts in this whole creation.

### inbox

The inbox is some kind of storage others can deposit information for the bot in. The data should contain some meta foo, such as information on who send the information to the bot as well as when (this would allow the bot to contact the sender in case some error happens or so).

### outbox

The outbox can be seen as some kind of public server. The bot can host arbitrary data there for others to download (for example results or so).

### project specific bots

Now a bot could do something like scanning a site for a specific vulnerability or so, but in the end, there could also be some kind of bot we could send information we want to distribute to others.

For example: say we're working on a project and find some interesting endpoint. There are a few options that can be taken from here on:

- Ping other users by directly sending them the information.
- Publish the information in the outbox for others to "scrape".

This would allow a bot that often receives information from another bot to "subscribe" to the initial bot and just extract the information from there

### interface

Interacting with the bots or the overall network should be possible using some kind of website, or even cooler, some tui.

What I imagine would be some kind of interface showing me the tasks of the bots, how many tasks are in queue, how much the've posted for others to view.

In the end, there should be a few bot's I actually "follow" which for example present me a new POC or some kind of error messages (the bot-council-bot which periodically tells me that some bot needs time off or so).

### fun

Another nice thing would be to make this completely public and some kind of mastodon instance, so that people could look at this "artwork" in which some bots are hacking stuff together with people. Some bot's might periodically post some random SQLi payloads or so which you could follow.

I'm still unsure if this is really a good idea, so I'm going to start off by keeping this totally private.

## negative

Now this could be quite fancy, but there are of course problems that might arise: It is super slow, the bot's will take some time to "communicate" and a lot of stuff might break.

## positive

The concept of introducing humans to the loop might really be something I'd like to see.