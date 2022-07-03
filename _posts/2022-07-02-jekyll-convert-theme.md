---
layout: post
title:  "Convert a Jekyll Gem-Based Theme to a Regular Theme"
date: 2022-07-02 00:00:00
category: Web Development
tag: Jekyll
---

# Convert a Jekyll Gem-Based Theme to a Regular Theme

Note that if you convert a gem-based Jekyll theme to a regular theme that lives in your website's directory, you won't receive theme updates.

To convert your theme:

1. Find the location of the gem directory. In a terminal or command line window, enter `bundle info --path minima` (replace `minima` with the actual name of the theme).
2. Copy all the folders from the gem's directory into your Jekyll site directory; no need to copy over the `LICENSE.txt` or `README.md` files.
3. Find the runtime dependency plugins used by the theme:
	- The plugins will be in the theme's `.gemspec` file, which should be in the `specifications` folder of your Ruby installation directory (e.g., `/usr/lib/ruby/gems/3.0.0/specifications/minima-2.5.1.gemspec`).
	- The plugins you're looking for will should look something like the following:
		`s.add_runtime_dependency(%q<jekyll-feed>.freeze, ["~> 0.9"])`
		`s.add_dependency(%q<jekyll-seo-tag>.freeze, ["~> 2.1"])`
4. In your Jekyll website folder, open the `Gemfile`. In the `group :jekyll_plugins do` section, add references to the runtime plugins like so:
	`group :jekyll_plugins do`
	  `gem "jekyll-feed", "~> 0.12"`
	  `gem "jekyll-seo-tag", "~> 2.7"`
	`end`
	Note: If one or more of the plugins are already listed in the `Gemfile`, just leave them in place.
5. In the terminal, enter `bundle update`.
6. In your Jekyll site, remove the reference to the theme gem:
	1. Open the `Gemfile` and remove `gem "minima", "~> 2.5"`.
	2. Open `_config.yml` and remove `theme: minima`.