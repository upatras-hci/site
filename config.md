# Welcome to Jekyll!
#
# This config file is meant for settings that affect your whole blog, values
# which you are expected to set up once and rarely edit after that. If you find
# yourself editing this file very often, consider using Jekyll's data files
# feature for the data you need to update frequently.
#
# For technical reasons, this file is *NOT* reloaded automatically when you use
# 'bundle exec jekyll serve'. If you change this file, please restart the server process.

# Site settings
# These are used to personalize your new site. If you look in the HTML files,
# you will see them accessed via {{ site.title }}, {{ site.email }}, and so on.
# You can create any custom variable you would like, and they will be accessible
# in the templates via {{ site.myvariable }}.
title: 'MSc HCI - UPatras'
email:
description: 'unoficial web site' 
url: "https://upatras-hci.github.io"
baseurl: "/site"
repository: "upatras-hci/site"
twitter_username: # username
github_username: # username
minimal_mistakes_skin: default
search: true

# Build settings
markdown: kramdown
remote_theme: "mmistakes/minimal-mistakes@4.21.0"
# Outputting
permalink: /:categories/:title/
paginate: 5 # amount of posts to show
paginate_path: /page:num/
timezone: # https://en.wikipedia.org/wiki/List_of_tz_database_time_zones

# Exclude from processing.
# The following items will not be processed, by default. Create a custom list
# to override the default setting.
# exclude:
#   - Gemfile
#   - Gemfile.lock
#   - node_modules
#   - vendor/bundle/
#   - vendor/cache/
#   - vendor/gems/
#   - vendor/ruby/

# Plugins (previously gems:)
plugins:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jemoji
  - jekyll-include-cache


footer:
  links:
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/"

# Collections
collections:
  people:
    output: true
    permalink: /people/:path/
  courses:
    output: true
    permalink: /courses/:path/
  pages:
    output: true
    permalink: /:path/
  news:
    output: true
    permalink: /news/:year/:month/:day/:title/

defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: true
      related: true
  # _pages
  - scope:
      path: "_pages"
      type: pages
    values:
      layout: single
      author_profile: true
  # _people
  - scope:
      path: ""
      type: pages 
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: true
      share: true
      related: true
  # _courses
  - scope:
      path: ""
      type: courses 
    values:
      layout: courses


category_archive:
  type: liquid
  path: /categories/
tag_archive:
  type: liquid
  path: /tags/

theme: jekyll-theme-minimal