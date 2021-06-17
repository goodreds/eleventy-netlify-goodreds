---
title: "5 Tools To Speed Up CSS Development"
date: "2013-10-09"
journal: "001"
metaDescription: "5 tools to speed up your development of CSS"
permalink: "/journal/5-tools-for-css/"
categories:
  - "code"
  - "how"
tags:
  - "news"
coverImage: "/static/img/code-e1580368194543.png"
---

**Date** {{ date | readableDate }}
**Journal Entry** {{ journal }}

{{ metaDescription }}

![code](images/code-620x242.png)

This article is not intended to explain everything but enough to make it possible to appraise your CSS workflow and hopefully see where you might want to head towards in the future.

### Live editing on the server

Chance of losing data. 'Seat of the pants' workflow! I know, you like to live life on the edge but NO, stop right there! Whilst useful for the smallest of edits due to its ease and speed, this is not the way to make CSS edits. Believe me, once an FTP glitch leaves you staring at a corrupted copy of your CSS you will not be happy trying to rebuild everything from scratch. But, you say 'I already took a copy' just to be safely protected against this exact eventuality. Fair play to you for being organised, although you doubtless have multiple CSS files called names like styles\_backup.css, styles\_not\_this\_one.css, styles\_old.css, styles\_definitely\_this\_one.css. Keeping track of all of these extra files is no way to a life of simple CSS edits, which is what you thought you were getting in the first place.

### Using dedicated software

- **CSSEdit** - fully featured Mac app. Occasionally buggy. Tricky to flip from x-ray mode to code all the time. Feels most creative (similar to Photoshop). Slow to update to CSS3 specs (border-radius etc) can be frustrating.
- **Coda** - fully featured Mac app. Bugs and waiting for updates can become tiresome
- **Dreamweaver** - full WYSIWYG editor on Mac & Windows.

Increases distance between you and your code as you're dependent upon the developer to add any new features. A lack of control over your own code and the endless clicking and Cmd-Tabbing changing window focus can make this a rather more onerous task for CSS editing than you were undoubtedly aiming for when you were being dazzled by the marketing copy on the sales page. That's not to say that these tools don't have a place but that as you develop your skills the limitations begin to outweigh the advantages.

### Text Editor™ & FTP app

Your own choice of simple text/code editor with a dedicated FTP app. This is simple, effective and allows you to upload at a time of your choosing. Still, some common sense is required to ensure no mistakes are made, such as overwriting files with similar names in the incorrect directory. Also this technique can be onerous to setup unless you know what you're doing from the outset - remote mapping of directories is not as fun as it undoubtedly sounds and I know of quite a few developers who ultimately end up working from a folder on their desktop rather than lay the groundwork for a stable, repeatable file structure from the outset.

### Sublime Text, Sublime SFTP plugin & Livereload

Sublime Text is an app available for Mac/Windows and unusually Linux and it is gaining a lot of traction in developer circles as the go-to editor of choice for a lot of people. Unusually it is easy to setup whilst still allowing for huge extensibility via the Package Control (think plugins for almost every development scenario). One of the most useful plugins is Sublime SFTP by Will bond. For a mere $20 this plugin does away with the need to rely on a separate FTP app as you can handle pretty much most file handling between the code editor and the server inside Sublime Text. When I say most file handling it enables you to do basic things such as setting the remote path (so your files go where you expect) and upload on save to more esoteric functions such as remote server time offsets, remote encoding and a whole host of regex functions enabling you to ignore certain file types so they are not uploaded to the server (i.e. Photoshop / Illustrator documents etc). The setup file is a standard JSON file that is human-readable and very simple to see what options are available. Ones you don't require are simply commented out. Any coder will be very happy with the setup, I'm sure. Livereload (or Codekit app) handle the automatic refreshing of pages. When you save in Sublime Text, SFTP uploads the changed document to the server and Livereload refreshes either the whole page or just the bits changed. You have control over which parts of your page refresh Livereload touches and also any time offset to enable the document time to upload prior to the page refresh.

### Livestyle (Emmet)

LiveStyle is a plugin that is currently in development that allows roundtrip CSS editing on the fly between Sublime Text and either Chrome or Safari (strictly Webkit nightly for now but Safari proper when OSX Mavericks is released). This is probably getting quite close to [fixing our web workflows](http://kenneth.io/blog/2013/05/21/our-web-development-workflow-is-completely-broken/) as it ensures changes made either in the Web Inspector of either browser and/or Sublime Text are refelected immediately within both the browser and code editor. In combination with the aforementioned Sublime SFTP plugin it begins to feel almost invisible from your brain/fingers to the reflected code in the browser and once my tools begin to recede into the background I think this is how it should be.
