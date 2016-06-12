TK present

would have been cool in the 80s
===============================

A minimalist, sort of retro theme.  Objectives are:

* Simple to adapt/maintain
* Fast loading with minimal dependencies (no scripting)
* Not entirely ugly - probably the weak link, let's be honest

The theme was inspired by the following geometric shapes to whom all credit is owed:

* All right-angled quadrilaterals
* The fillet (but not the chamfer)

A live site using this theme: [socratic.space](http://socratic.space) (warning: it's terrible)

## Screenshot

![WHBCIT8 screenshot](https://raw.githubusercontent.com/pedrodude/would-have-been-cool-in-the-80s/master/images/screenshot.png "WHBCIT8 screenshot")

## Installation

Generic installation instructions are [here](https://gohugo.io/themes/installing/)

## Setup

### Site configuration

To "make it yours" (even though we all know this theme is *mine*), change the bits of the following toml file that start with TK (and get rid of the TK)

---
```toml
#Adjust all settings that start with TK to customise this theme to your site.  Also remove the TK
theme = "would-have-been-cool-in-the-80s"
baseurl = "TK http://mysite.com"
languageCode = "en-us"
title = "TK MY SITE'S TITLE"

[params]
  aboutpage = "TK name-of-the-about-post" #This makes the "about" link in the header function.  It must be the exact filename of your about page without the file extension.  E.g. if your about page is called "mysiteabout.md" then enter in "mysiteabout"
  author = "TK Your Name" #Goes in the meta info of your webpage to help identify you as the author of the content
  copyrightstatement = "TK A copyright statement of your choosing." #Will appear in the footer of each page.
  description = "TK A description that will appear in the html meta" #Goes in the meta info of your webpage to describe the content of your site
  siteclass = "TK MY SITE'S SUBTITLE" #Optional.  If you set it, it will display a subtitle in a contrasting color (adjustable within the CSS) on the site's index page.
  tagline = "TK My site's witty tagline" #Optional.  If you set it, it will display a tagline for the website underneath the titles.  By default it appears italicized.
```
---

### CSS

The CSS is adapted from [HTML5 Boilerplate](http://gohugo.io).  Just a few layout and color tweaks.  There are some override styles and a few custom ones prefixed with "whbcit8".  In terms of font choice: geometric sans-serifs, monospace, and perhaps even slab serifs all seem to work fine.

That's about it.  I could have done more I'm sure with pagination and all that crap but I was basically going for one step beyond a MVP, as well as teaching myself HTML5 and CSS3, and this Hugo thingy.

### Individual page configuration

Page configuration is largely unchanged from the default but there are some additional bits in the archetype (the template that defines default page settings) which enable additional features.  It's explained in the comments in the toml file below.

---
```toml
+++
streamtitle="" #Optional.  If you set it, it will display a subtitle in a contrasting color (adjustable within the CSS) on the individual page.
timeless = "false" #Optional.  If you set it, it will determine whether the post displays date features (displaying a date on the post summary on the index page, date in the page title).  Changing the value to true suppresses all of these features, with the exception of the last modified date shown by the pedrolastmod parameter
draft=true
pedrolastmod="YYYYMMDD" #Optional.  If you set it, it will display a Last Modified Date under the footer.  This is not automated at all, nor formatted, but simply provides a basic ability to indicate that the creation date differs from the modified date.  If left unchanged, it will display the created date.
+++

LOREM IPSUM PAGE CONTENT GOES HERE
```
---

## Dependencies

### HTML5 Boilerplate [and Normalize.css]

Ok so I didn't do all of this theme myself.  I did have to embarrassingly rely on [HTML5 Boilerplate](https://html5boilerplate.com/) and [normalize.css](https://necolas.github.io/normalize.css/).  For a beginner like me these are absolutely amazingly brilliant bits of work.  Although I was utterly dismayed to find that a shim like normalize.css was necessary.  Seriously, wtf?  Isn't there like a W3C, or perhaps ISO to tell people how to make a consistent renderer.  I know that as a neophyte I probably sound completely ignorant here, and also that there's a ton of history behind this.  But goddamn.  Wouldn't have had this problem in Soviet Russia... nor perhaps the money for a computer but whatever.  These things meant I had to think less, so thank you!

### Hugo

Is [Hugo](http://gohugo.io) itself a dependency?  I don't know what I'm supposed to put in this readme but duh, you need hugo to use this theme.  And again thank you for being like the normalize dudes and making a thing that didn't require me to think.  I roll Windows like a total web n00b and I'm usually using all my brainpower to not bump into things, so the fact I could just freaking download an .exe and not even have to add it to my path made me smile.  I mean I did stare for way too long trying to decide if I could use the 64-bit version or not (seriously, who calls it AMD64 anymore?! Just call it x64 like the rest of the world and stop trying to be cool, hugo dudes).  But yeah you are kind of cool, especially since I went to Jekyll first and they told me I needed some ruby gems...  Only my wife gets "ruby gems" (normal people just call them "rubies") from me... otherwise who has time for that shit.

### Google Fonts

The default configuration uses a rather nice geometric sans-serif font called [Montserrat](https://www.google.com/fonts/specimen/Montserrat) hosted by Google Fonts.

## And how I set it up

This is the least relevant part of the readme but I've included it as I think Hugo hasn't really made clear the benefits of using a Static-Site Generator (or Static CMS) such as Hugo.  Perhaps because the issue is bigger than them.  In my opinion these platforms are still too intimidating for most people to feel comfortable attempting.

So how about some advice from an idiot; yours truly.  My requirements were:
* Low-cost (cheaper than a typical hosted solution)
* Relatively simple (i.e. no programming or any other complex technical setup)
* High-level of control (i.e. no artificial limitations from the platform)

Here are some brief notes on the setup I found works best.  The skills you need are the ability to read the instructions and a bit of batch scripting [to use S3.exe]:
- Domain from [Gandi.net](http://gandi.net)
- DNS routing provided by [Amazon Route 53](https://aws.amazon.com/route53/)
- Storage provided by [Amazon S3](https://aws.amazon.com/s3/)
..-S3 uploading provided by [S3.exe](https://s3.codeplex.com/)
- CMS website generation provided by Hugo