# ecosystem

The <a href="/projects/lun">lun</a> project is supposed to be a project to learn stuff, but in the end, I actually want to build more than a programming language... ...a whole ecosystem.

Now this blogpost is just me writing some thoughts down, so this might be interesting or not, depending on how readable this is going to be.

## base idea

- infra for all

## components

- <a href="/projects/kosali">kosali</a>: hack-dashboard 0.1
- <a href="/projects/navoge">navoge</a>: hack-worker 0.0
- <a href="/projects/bizago">bizoga</a>: hack-manager 0.0
- <a href="/projects/bodula">bodula</a>: code host 0.0
- <a href="/projects/pehafo">pehafo</a>: code search 0.0
- <a href="/projects/luxaki">luxaki</a>: ci/cd 0.0
- <a href="/projects/wemoba">wemoba</a>: hack-frontend 0.0
- <a href="/projects/kinudu">kinudu</a>: 

## hack

I want some frontend I can throw some resouce (URL/binary/...) in which passes it to the workers which can then use it, work with it, share information on it and other stuff. Now these workers might not only be "bot" (as in programs), but also the "real" people.

### kosali

The hack-dashboard. This is supposed to be the main place to look into if we want to get informationo on what is happening somewhere.

- **movable**
  Say I'm running something locally, I want to be able to stop it, move the script and the state to some other machine and continue there.
- **pure**
  When running a script, the hash of the build env should be stored
  