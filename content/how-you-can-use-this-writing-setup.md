+++
title = "How you can use this Writing Setup"
date = 2025-10-29T20:14:52+05:45
[taxonomies]
tags = ["tutorial"]
+++

Let's start from the beginning. I made this blog to write stuff daily without giving too much thoughts on it, to  see my progress on topics that may be controversial and how I am improving on it. [_Things that I have a very crude understanding of but still have opinions on._]

I basically have two personas here, one the writer me and another the commenter/explainer me. [_Hey! that's me!_] So, judging me entirely by this blog alone will be like judging a kid for making mistakes.

## Interactions 

Blabbering in the wind just doesn't cut it for a learning process. This might calm me down but it wont give me clarity. I might get clarity by researching things by myself but I want a natural approach. Someone envisioned that communnications in the web can also be decentralized as well as interactive and drafted the concept of webmentions, and that resonated with me. As opposed to communicating via a social media being limited to their visual design, I wanted something that had structure but still can be personalized. 

I decided to make this into a template and not just my personal site because I found out that there aren't many people who use webmentions as a form of communication. And if there are, they aren't someone who would interact to my silly ramblings. Also, this site is heavily inspired by [Manu's](https://manuelmoreale.com/thoughts/welcome-to-manus-website) site because of it's simplicity [_(I don't credit him enough, this design it so brilliant.)_], but I added a bunch of complexities to it.

## Characterstics

1. Built with [zola](https://www.getzola.org/) static site generator. [_Because it is rust, and is easy to install and use than hugo._]
2. Simple and uses my hand written CSS [...again! Inspired by [Manu's](https://manuelmoreale.com/thoughts/welcome-to-manus-website) blog.] and no JS.
3. Has tags to categorize posts. [_Because, https://webmention.app/docs#using-the-command-linewhy not?_]
4. Uses [webmention.io](https://webmention.io/) as the listener for webmentions.
5. [webmention.app command line](https://webmention.app/docs#using-the-command-line) and zola generated RSS feed for sending webmentions.
6. [GitHub Pages](https://docs.github.com/en/pages) and [GitHub Workflows](https://docs.github.com/en/actions/concepts/workflows-and-actions/workflows) for hosting and checking the webmentions periodically.
7. A custom style for [_"inner voice"_] which you can use while writing the post. `[_Hi_]` becomes [_Hi_].

[_Though I like to shit on GitHub for being a monopoly and for being Microsoft, I can't deny the fact that they give free access to workflows and pages._]

Though the default CSS and layout is good, I encourage you to tweak the layouts [_(/templates)_] and change the CSS to make it personal to you.

## Step by Step Instructions

> **1. Fork and clone [this](https://github.com/scientiac/blog.carboxide/) repo.**
>```sh
> https://github.com/scientiac/blog.carboxide
> ```

***

> **2. Make it yours.**   
> 1. Edit `config.toml`  with your information [_getthing the URLs wrong will result in pages not linking properly_] and fill everything correctly.  
> [_Email is necessary for creating and verifying your indieweb account._]  
> 2. Edit the `/static/CNAME` with your domain and replace `/static/thumbnail.png` with your profile picture.
> 3. Make sure to install [zola](https://www.getzola.org/) on your system and test the site locally using `zola serve`.  
> 4. Edit the files in `/author` and `/now` to write about yourself.
> 5. If everyting is correct push the changes to the GitHub repo.

[_In the config you can use themes for syntax highlighting from [the zola docs](https://www.getzola.org/documentation/getting-started/configuration/#syntax-highlighting)._]

***

> **3. Give GitHub actions the necessary permission to write to your repo.**   
> Go to `Settings > Actions > General > Workflow permissions` and select `Read and write permissions`.  
> Re-run the workflow if it had failed previously.

***

> **4. Run the workflow and then enable the pages.**  
> After the GitHub action successfully runs, go to `Settings > Pages > Build and Deployment` and select `Deploy from a branch` on `Source` and `gh-pages` & `\root` on Branch.
> Add your domain name to `Custom domain` if you have one.

*** 

> **5. Check if the site is published.**  
> Go to the website and see if everything is working properly. Only if your website is published go to the next step. 
> Verify your `h-card` on [indiewebify.me](https://indiewebify.me/validate-h-card/) and see if everything is correct.

*** 

> **6. Make a webmention.io account.**  
> Go to [webmention.io](https://webmention.io) and put your website URL in there. 
> It will automatically detect your email address. Then, verify your email to log in.
> Go to `settings > API Key` and copy it to your clipboard.

*** 

> **7. Save your API secret on GitHub.**  
> Go to GitHub `Settings > Secrets and variables > Actions > Repository secrets` and click on `New repository secret`.  
> Add `WEBMENTION_TOKEN` as the `Name` and the API key you copied as the `Secret` then click on `Add Secret`.

*** 

> **8. Add the proper workflows.**  
> After you have the page working and webmention.io set up. Remove the current workflow.  
> Then move the workflows directory from the root to `.github`.
> ```bash
> # from the project root
> rm -rf ./.github/workflows/
> mv ./workflows/ ./.github/
> ```
> And finally push the changes.

*** 

> **9. Verify that everything is working correctly.**  
> Check if all the GitHub actions run successfully and nothing fails.
> Verify everything in [indiewebify.me](https://indiewebify.me). [_It is fine if **Syndicated Copies** shows an error._]

*** 

> **10. Finally write your posts.**  
> Write your posts by making a markdown file in `/content` with the proper header like in the example `/content/one.md`.  
> If you use Nix then use `direnv` to enable the nix shell which automatically installs zola for you. You also get a command called `now` that you can run to get the properly formatted datetime for the post.

_If you write a post and try to push to the repo, it might fail because the workflow pulled the webmentions from webmentions.io and merged it to your repo. It is fine to force push to publish the changes. If not, then remember to pull and merge the changes before you push._


## Sending Webmentions
In order to send Webmentions, the content should be formatted accordingly. In general I like to utilize three activities to send Webmentions.
[_It is preferred to only use one activity for one mention._]

### Mention
One can mention a site using webmention by simply putting the link to the page being mentioned.
The site will get the webmention if it supports it.

```md
[I love learning things](https://faulty.carboxi.de/learning/) by faulty.
or
<a href="https://faulty.carboxi.de/learning/">I love learning things</a> by faulty.
```

### Like
One can like a post using webmention by formatting the link as follows:

```md
I like how faulty talks about learning in <a class="u-like-of" href="https://faulty.carboxi.de/learning/">I love learning things</a>.
```

I like how faulty talks about learning in <a class="u-like-of" href="https://faulty.carboxi.de/learning/">I love learning things</a>.

### Reply
One can reply to a post by formatting the link and the text as follows:

```md
<a class="u-in-reply-to" href="https://faulty.carboxi.de/learning/">I love learning things</a>

I feel the same about learning. Nice writing faulty!
```

## Finally

I made this to introduce people to webmentions and increase interactions using it. I encourage writing both goofy and serious stuff. [_And even stupid stuff._] And most importantly I incourage people to customize the hell out of this base, changing and tweaking css and html without breaking the indieweb structure.

[_Happy writing!_]
