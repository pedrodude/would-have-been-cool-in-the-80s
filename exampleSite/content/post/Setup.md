+++
coolinthe80slastmod = "YYYYMMDD"
date = "2000-01-03T12:00:00+02:00"
draft = false
streamtitle = "Explanatory Notes"
timeless = "true"
title = "Setup"

+++

## Installation

Generic installation instructions are [here](https://gohugo.io/themes/installing/)

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