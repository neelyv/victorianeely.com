---
layout: post
title:  "Use Notepad++ to Pull a List of URLs from an HTML Document"
date: 2022-08-06 00:00:00
category: Text Editing
tag: Jekyll
---

# Use Notepad++ to Pull a List of URLs from an HTML Document

Recently I needed a way to take all the URLs from an HTML document and paste them into a spreadsheet. There were far too many to do by hand; I needed some sort of automated solution. After some Googling, I found what I was looking for on <a href="https://superuser.com/questions/1536915/notepad-inverse-regex-replace-all-but-string">superuser.com</a>: Paste your text into Notepad++ and use bookmarking to remove all but the strings you want to keep. I took those steps and adapted them for my purposes:

1. Copy and paste the HTML markup into Notepad++.

2. Select <code>Search &gt; Mark...</code>, and then check <code>Bookmark line</code>.

3. Under "Search Mode", make sure <code>Regular expression</code> is selected.

4. For "Find what:", enter: <code>^.*(?:href="http).*$</code>

5. Select <code>Mark All</code>.

6. Select <code>Close</code>. All the lines containing href links will now be highlighted.

7. Select <code>Search &gt; Bookmark &gt; Removed Unmarked Lines</code>. This will remove all but the highlighted (bookmarked) lines.

8. You'll still have extraneous markup to remove. To begin removing all text except for the URLs, press <code>Ctrl-H</code>.

9. Make sure <code>Regular expression</code> is selected.

10. For "Find what", enter: <code>^.*href="(.*?)".*?&gt;.*?$</code>

11. For "Replace with", enter: <code>$1</code>

12. Select <code>Replace All</code>.

You should now have a clean list of URLs.