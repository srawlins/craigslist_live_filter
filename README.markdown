A Greasemonkey User Script
==========================
v 1.2

Summary
-------
This script adds a filter-out box, fixed in the bottom right of all craigslist pages. It allows you to type in words you wish to filter out of the current results. Oh, it also sets all listings to ALL LOWERCASE. If I wanted to be harsh, I would just filter out any listings with a single word written in all caps. Gah! And the filter text and options are persistent, even if you close your browser.

Features at a glance:

+ downcase all letters in all listings
+ filter out listings by regex or by lists of words
+ gray out filtered-out listings, or hide them
+ persistent settings and filter text (uses Greasemonkey's storage)

How to Use
----------
There are two ways to list the content that you want filtered out.

+ First is with regex (regular expressions). This is a sweet feature, but personally I've been using the second way.
+ The second way is with words, comma-separated. You can simply list terms you wish to filter out, like so:

Examples
--------

+ In "words" mode, "apartment, 1ba" will filter out all listings with the term "apartment" or with the term "1ba".
+ In "words" mode, "vail" will unfortunately filter out all listings with the term "vail", including any with the word "available". :( **It is not a whole-word-only filter.**
+ In "regex" mode, "\Wvail" will filter out listings with terms such as "(vail" and " vail", but not "available" ("\W" is regex for a non-word character).
+ In "regex" mode, "apartment|1ba" gives the same results as the above "words" mode example.
+ In "words" mode, "oro valley, loma linda" will filter out all listings with the term "oro valley" or with the term "loma linda"; spaces are fair game within a term; **commas** are used to separate terms.
+ In "words" mode, you can secretly add most forms of regex as well: "\Wapt\W, \Wvail\W, ranch" will search for the term "ranch" and the terms "apt" and "vail" with non-word characters surrounding them (thus *not* matching "aptitude" or "available").

Filter-Out Display
------------------
You can also choose how filtered-out listings are displayed. The two choices are:

+ Gray: Gray out listings, and highlight the term that caused the listing to be filtered out.
+ Hide: Hide the filtered-out listings.

Todo
----

+ Drop down to view more than one page of listings.
+ Other UI tweaks, like listing $/month/person or something...
+ X out listings as you go.
+ Date separaters
+ I'm noticing a performance lag when I have > 60 words filtered...

Changes
-------

v 1.2

+ Tweaked performance
+ Fixed so only displays on search results pages

v 1.1

+ Added filtered-word highlighting

v 1.0

+ initial release