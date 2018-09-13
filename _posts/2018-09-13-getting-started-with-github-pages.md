---
layout: post
author: justin
title: "Getting Started With GitHub Pages"
---
I'm hoping to document the things that I set up for this blog well enough so that anyone trying to do the same things can struggle less than I did. Plus, I like the idea of having a blog that contains meta documentation. You can do it too!

I decided to use [Github Pages](https://pages.github.com/) because it seemed pretty simple. It uses [Jekyll](https://jekyllrb.com/) which is a static site generator so there's not a lot involved on the server-side. Also, GitHub Pages builds your site from a GitHub repository so you get the benefit of always having a backup of everything you do, and you can do cool things like allow your readers to submit pull requests for any mistakes that they find. There's a cool way to include "Improve this page" links (for pull request submissions) on every page automatically too.

Another reason for using GitHub Pages was to get away from the maintenance involved in using WordPress--the platform this site was previously built with. WordPress didn't really work for me because I didn't pay it enough attention to keep it updated or even running. My blog kept going down, and, after a while, I forgot to keep fixing it. It wasn't ideal for me. I'm hoping that GitHub Pages will just work, and that it's simple enough to be able to come back to and be effective with after forgetting about it for some time.

Anyway, enough talk about why. Let's get to the meat of this. My goal was to set up GitHub Pages and use a custom domain name so that I could use my old website's domain name. I.e. I wanted justpushbuttons.com to display my personal GitHub Pages site (which by default is jlvallelonga.github.io).

In order to document the process, I used another domain name and a second GitHub account so that I could make sure I had everything correct. I was hoping that it would run smoothly the second time I did it, but that didn't really happen that way. I think I have it figured out now though. I'll try to document things well enough so that you can avoid the trouble that I ran into.

So the domain that I used was notasecondlate.com. Get it? Like, my name is Justin. Sometimes people say "Just-in-time" and then laugh like I haven't heard that 1000 times before. So "not a second late" is like... you see... ok whatever.

I started by creating a GitHub account with the username "notasecondlate". That's pretty [straightforward](https://github.com/). Then I followed the instructions on the GitHub Pages homepage which are great so I'll leave you to reference that here:
[https://pages.github.com/](https://pages.github.com/)

After following their instructions, my GitHub Pages site wasn't working:

![](/assets/img/github-pages-404.png)

but it said that it was working:

![](/assets/img/settings-site-published-message.png)

I found out that you can use a markdown file as your index page so, to troubleshoot, I renamed `index.html` to `index.md` and then I got this:

![](/assets/img/notasecondlate-basic-theme.png)

Ok, it was working, but I didn't really want that big blue header. So I renamed the file back to `index.html` and now magically it worked:

![](/assets/img/halo-world.png)

Ok that was weird, but whatever. So if you happen to run into the same problem then you can try what I did. Apparently [I’m not the only one with this issue either](https://github.community/t5/GitHub-Pages/index-html-not-working/td-p/1266)

The site may have still been generating when I tried to visit the first time, so being patient is worth trying as well. I'm not really sure how long you should expect GitHub to take to get your site running, but it didn't take long with the first site I set up--maybe 10 minutes at the most.

If you don't want a custom domain name, then that's all you need to do. You can start customizing your site. The [Jekyll step-by-step tutorial](https://jekyllrb.com/docs/step-by-step/01-setup/) helped me get up to speed on the basics. To set up a custom domain name, continue reading.

So now I had my GitHub Pages site running at notasecondlate.github.io. To get notasecondlate.com pointed at this site (meaning visiting notasecondlate.com will load the GitHub Pages site), I just needed to add some DNS records. I bought notasecondlate.com from [Namecheap.com](https://www.namecheap.com/). They include DNS services when you register with them so I didn't have to use a different service for this.

When I initially tried to set this up, something went wrong and the website wasn't loading or doing HTTPS redirects correctly or something. I didn't document it very well so I'm fuzzy on details here. I think the best thing to do is to follow the steps carefully in order. When I did that, everything worked out.

I mostly followed the steps on this page for [setting up a custom domain name with Namecheap](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages)

The main difference was that instead of manually creating a CNAME file, I let GitHub do it for me. To make that happen, I went to the project settings on the GitHub repo:

![](/assets/img/project-settings.png)

Then in the GitHub Pages section, under "Custom domain", I entered "notasecondlate.com" and then clicked "Save"

![](/assets/img/custom-domain.png)

This adds the CNAME file to the GitHub repo for you.

The next step is to add the DNS records with Namecheap's advanced DNS settings. You can follow steps 2 and 3 [on this Namecheap GitHub Pages guide](https://www.namecheap.com/support/knowledgebase/article.aspx/9645/2208/how-do-i-link-my-domain-to-github-pages) to get that working.

I had 2 conflicting records that I removed (they were there by default):

![](/assets/img/namecheap-conflicting-dns-records.png)

So your DNS settings should look something like this when you're finished:

![](/assets/img/namecheap-advanced-dns-records.png)

The last thing to do is to enforce HTTPS (if it isn't already). Under the project settings for your repo, under the "GitHub Pages" section, check the "Enforce HTTPS" checkbox

![](/assets/img/github-settings-enforce-https.png)

You will have to wait some time before the DNS changes propagate, but come back in a day or two and your site should be up at the custom domain that you set up! Let me know in the comments if you have any questions or issues with the process of setting up your site. Or submit a pull request to suggest a change.

Thanks for reading!
