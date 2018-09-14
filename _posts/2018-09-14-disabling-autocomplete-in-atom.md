---
layout: post
title: "Disabling Autocomplete In Atom"
---
I use [Atom](https://atom.io/). It’s kind of buggy, but I love it because of the customization options that you get with it. It definitely has some annoying bits though. I should contribute to the project, but until then I’m finding some workarounds to make my programming life a bit less annoying.

One thing about Atom that I’m not particularly fond of is the autocomplete feature. Maybe some people find it useful, but I’m not one of those people. When I’m typing away (mostly when I’m writing and not coding) and I hit “tab” or “enter” and some random autocomplete suggestion gets filled in, I find it pretty frustrating. It’s even worse when the suggestion is a code snippet, and a few lines of random code are placed right by my cursor.

So anyway I disabled it. Here’s how:

Go to the Atom Settings:
Atom > Preferences...

![](/assets/img/atom-preferences.png)

Or just hit `Cmd+,`

Then go to "Packages":

![](/assets/img/atom-packages.png)

Then find “autocomplete-plus” and click “Settings”

![](/assets/img/atom-autocomplete-plus-package.png)

Then uncheck the “Show Suggestions On Keystroke” checkbox:

![](/assets/img/atom-autocomplete-plus-show-suggestions-on-keystroke.png)

That's it!
