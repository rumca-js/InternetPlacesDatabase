﻿# Overview

This is a database of Internet places. Mostly domains. Sometimes other things. Think of it as Internet meta database. This repository contains link metadata: title, description, publish date, etc.

<div align="center">
  <img alt="Project Logo" src="images/its_easy_internet_on_internet.png">
</div>

# Acceptable link types

 - domains
 - repository links. For example [https://github.com/rumca-js/Internet-Places-Database](https://github.com/rumca-js/Internet-Places-Database)
 - user spaces. Might be youtube channel link: [Linus Tech Tips YouTube Channel](https://www.youtube.com/channel/UCXuqSBlHAE6Xw-yeJA0Tunw). Might be X/Twitter user account.

# Not acceptable link types

 - content farms
 - malware sites
 - porn, casino, etc.
 - it infrastructure domains, CDN domains
 - analytic domains that are used for user surveillance, not to provide data

I do not always follow these rules strictly. There are exceptions for some domains. Some sites are allowed to be in database, but are down-voted.

# Sources of data

Obtained by the [Django-link-archive](https://github.com/rumca-js/Django-link-archive) web crawler.

Sources:

 - [https://nownownow.com/](https://nownownow.com/)
 - [https://searchmysite.net/](https://searchmysite.net/)
 - [https://downloads.marginalia.nu/](https://downloads.marginalia.nu/)
 - [https://aboutideasnow.com/](https://aboutideasnow.com/)
 - hacker front page entries
 - some reddit channels [r/selfhosted](https://www.reddit.com/r/selfhosted/.rss)

# Files

The database is distributed as a set of JSON files. We do not want to store binary data, binary files. SQL files should be fine, but I am going with JSON files for now.

Each link contains a set of attributes, like:
 - title
 - description
 - page rating
 - date of creation
 - date of last seen
 - etc.

# Page rating

Content ranking is established by the [Django link archive](https://github.com/rumca-js/Django-link-archive) project.

To have a good page rating, it is desireable to follow good standards:
 - [Schema Validator](https://validator.schema.org/)
 - [W3C Validator](https://validator.w3.org/)
 - Provide HTML meta information. More info in [Open Graph Protocol](https://ogp.me/)
 - Provide valid title, which is concise, but not too short
 - Provide valid description, which is concise, but not too short
 - Provide valid publication date
 - Provide valid thumbnail, media image
 - Provide a valid HTML status code. No fancy redirects, JavaScript redirects
 - Provide RSS feed. Provide HTML meta information for it [https://www.petefreitag.com/blog/rss-autodiscovery/](https://www.petefreitag.com/blog/rss-autodiscovery/)
 - Provide search engine keywords tags

Your page, domain exist alongside thousands of other pages. Imagine your meta data have an impact on your recognition, and page ranking.

Remember: a good page is always ranked higher.

You may wonder, why am I writing about search engine "keywords" meta field, if Google does not need them. Well I don't like Google. If we want alternative solutions to exist, it should be possible to easily find your page from simpler search engines. Provide keywords field if you support open web.

# Tags

Each entry can be tagged. Most notable examples of tags

 - open source - if entry is "open source" related
 - personal - if it seems to be a personal website
 - self-host - software that can be self-hosted
 - company - if entry exists just to provide information about company
 - university, museum, etc - if entry provides details about a university, museum, etc.
 - disinformation / misinformation - self explanatory
 - news - if it is "news" content farm. Might be also "game news", "tech news", etc.
 - amiga - anything amiga related
 - wtf - for really interesting finds
 - link service - bitly or other services that provide shortened versions of links

# Notes

 - Not all domains have to be stored here. I think it would be best to have valuable domains. Certainly we do not want content farms. We do not need sites that do not contribute anything useful to the society, to the reader
 - The distinction is not that clear-cut, but more lenient rules apply toward personal sites
 - I am not that interested in marking substack, or medium as "personal" sites, as I do not feel that it should be tagged as such
 
# Demo database

Might not be working. Used for development: [https://renegat0x0.ddns.net/apps/places/](https://renegat0x0.ddns.net/apps/places/)

<div align="center">
  <img alt="Meme" src="images/bender.png">
</div>
