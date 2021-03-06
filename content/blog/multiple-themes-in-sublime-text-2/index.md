---
title: "Multiple Themes in Sublime Text 2"
date: 2012-11-07 15:09:00-0400
tags: [Productivity, Text Editors]
---

One thing I like to do is to have *different* themes for different file types in my text editor. That way, at a glance, I can guess what kind of file a text-filled window contains, especially when zoomed out using Mission Control. I've been using *Custom Language Preferences* in [BBEdit](http://click.linksynergy.com/fs-bin/stat?id=V41G*FiMqjc&offerid=146261&type=3&subid=0&tmpid=1826&RD_PARM1=https%253A%252F%252Fitunes.apple.com%252Fus%252Fapp%252Fbbedit%252Fid404009241%253Fmt%253D12%2526uo%253D4%2526partnerId%253D30) preferences to set up the color scheme for each file type there. *[TextMate 2](https://github.com/textmate/textmate) users, check out [Multiple Themes in TextMate 2](https://hiltmon.com/blog/2013/02/22/multiple-themes-in-textmate-2/).*


But how to do this in [Sublime Text 2](http://www.sublimetext.com)?

Turns out, it's easy. The file on the left is Ruby, the one on the right is Markdown (The sample code is [Slogger](http://ttscoff.github.com/Slogger/) by [Brett Terpstra](https://twitter.com/ttscoff)).

{{< figure src="images/sublime-two-themes.jpg" width=640 height=416 >}}

To achieve this, first install all the themes you may need. Obvious, I know!

{{< figure src="images/sublime-set-color.jpg" width=256 height=127 class="image-right" >}}

Then set the default theme using **Preferences / Color Scheme** from the **Sublime Text 2** menu.  This sets the theme in the default  preferences file which resides in **~/Library/Application Support/Sublime Text 2/Packages/User/Preferences.sublime-settings**.

The theme line looks like this in the file:

```
{
	…
	"color_scheme": "Packages/User/Railscasts.tmTheme"
	… 
}
```

Next, open a file type where you would like to use a *different* theme, for example, open a Markdown file. It will open using the default theme. Now choose **Preferences / Settings More / Syntax Specific - User** from the **Sublime Text 2** menu. Sublime Text 2 will create a new settings file with the selected file type as its name (in my case, the markdown settings file is **Markdown.sublime-settings**). If the file already exists, Sublime will open it for editing.  

Set the theme in this file, as well as any other settings you like for that file kind.  For example, my **Markdown.sublime-settings** is:

```
{
  "color_scheme": "Packages/MarkdownEditing/MarkdownEditor.tmTheme",
  "line_numbers": false,
  "font_face": "Cousine",
  "font_size": 13
}
```

You may need to restart Sublime Text 2 after this.

Next time you open a file where you have set type-specific user settings, the theme specified will be used. Nice!

See also [My Sublime Text 2 Setup](https://hiltmon.com/blog/2012/08/14/my-sublime-text-2-setup/) and [Multi-Platform Editing Is Sublime](https://hiltmon.com/blog/2012/11/26/multi-platform-editing-is-sublime/). And follow me at [@hiltmon](https://https://twitter.com/hiltmon) on Twitter or [@hiltmon](https://alpha.app.net/hiltmon) on App.Net.
