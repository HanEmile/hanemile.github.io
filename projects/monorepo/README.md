# monorepo

As described in the <a href="/blog/2021/07-12-monorepo">monorepo</a> blogpost, I looked into monorepos and thought of tranfserring a lot of stuff into them.

Now for this page, I'd like to make it a monorepo as well, although I'm not quite sure how exactly I'm going to do this. The problem here is that I'd like nice local repos with short urls (such as git.emile.space/vokobe), but also kind of "embed" them into the emile.space structure so that, using <a href="/projects/vokobe/">vokobe</a> as an example, the projects lay in emile.space/projects/vokobe. Now that I'm writing this, I'm realizing that this might actually work, due to this only being a remote.

Overall, I'm thinking of integrating a <a href="https://github.com/mmitch/git2html">git2html</a> like part into <a href="/projects/vokobe">vokobe</a>, so that each project as some web view and can be cloned from there. I've still got to figure out how to create such a git remote, as I've looked into it and it doesn't seem all to complicated, but the times I tried it it just didn't feel right.