# matrix-mail

After building my own <a href="/projects/matrix/matrix-sdk">matrix-sdk in golang</a> some time ago, I went on and built something in rust: a matrix-mail bridge.

It's actually quite a simple concept:

- I create a room
- I invite the bot (they join in a second or two)
- (Only I can invite the bot, as other invites aren't accepted, as the bot only
  "trusts" me)
- I send the bot commands to configure the recipients
- All messages sent in that room are sent via email to the recipients
- All responses get posted in the room from the bot

That way, I can write with people via email from within my matrix client.

## source

- <a href="https://git.sr.ht/~hanemile/matrix-mail">https://git.sr.ht/~hanemile/matrix-mail</a>
