---
layout: post
title: "Adding A Remote Theme To Your GitHub Pages Site"
---
I'll keep this one short and sweet since this process is pretty simple with [Jekyll](https://jekyllrb.com/). On this website, I'm using the [tale](https://github.com/chesterhow/tale) theme from [Chester How](https://chester.how/). The readme on this project gives you a pretty clear path to getting this theme installed so [I'll leave you to that](https://github.com/chesterhow/tale#installation) if you want to use the same theme.

There are a few options for installing themes with Jekyll. There's very complete documentation about Jekyll themes in [the documentation](https://jekyllrb.com/docs/themes/). There's also a very detailed write up on GitHub about [installing a theme on your GitHub Pages site](https://help.github.com/articles/adding-a-jekyll-theme-to-your-github-pages-site/). If you're wicked lazy like me then this post is for you!

To install a remote-theme, you can add a line like this to your `_config.yml` file and commit the change:

`remote_theme: chesterhow/tale`

Keep in mind though that doing _only_ this will _only_ work on your live GitHub Pages site. If you want to install a remote-theme and have the ability to preview the site locally, you'll need to add a couple additional things.

First you'll have to add the following to your `Gemfile`:

`gem "jekyll-remote-theme"`

Then you need to add this to your `_config.yml` file:

```
plugins:
  - jekyll-remote-theme
```

or if you already have a `plugins` section, then just add the `- jekyll-remote-theme` line under it.

After that you'll have to run `bundle` and then if you run `bundle exec jekyll serve` you should see your new theme installed on your local site at `localhost:4000`.
