---
layout: post
title:  "Create a Blank Jekyll Site"
date: 2022-07-02 00:00:00
category: Web Development
tag: Jekyll
---

# Create a Blank Jekyll Site

To create a new blank Jekyll site without any pre-installed themes:

1. Run the command `jekyll new sitename --blank` (replace `newsite` with the name of your site).
2. `cd` to your new website folder.
3. To install a Gemfile in your website directory, in a terminal or command line window, enter `bundle init`.  This will create your Gemfile for you.
4. To add Jekyll as a dependency, enter `bundle add jekyll`.
5. <strong>If you are using Ruby version 3.0.0 or higher:</strong> Add webrick to your dependencies with the command `bundle add webrick`. Otherwise, skip to the next step.
6. To serve your website locally, enter `bundle exec jekyll serve`
7. Go to your website at <code>http://localhost:4000/</code>.