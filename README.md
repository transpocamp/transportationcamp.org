**Looking for the TransportationCamp web site? Go [here](http://transportationcamp.org)!**

`transportationcamp.org` for TransportationCamp organizers
==========================================================
This document is intended to orient TransportationCamp organizers and 
The `transportationcamp.org` Web site is hosted using [GitHub Pages](https://pages.github.com/), a service of [GitHub](https://github.com/), a popular Web site for hosting software projects. GitHub is built around the [Git](https://git-scm.com/) distributed version control system (think Microsoft Word's _Track Changes_, only better), but for most things you won't need to interact directly with Git.  After creating a GitHub account and being granted access, you can edit pages on `transportationcamp.org` over the Web, without any special tools.  Most pages on `transportationcamp.org` are written in [Markdown](https://guides.github.com/features/mastering-markdown/), but you can also use HTML 

How to edit `transportationcamp.org`, condensed
-----------------------------------------------
0. [Create a GitHub account](https://github.com/join), if you don't already have one.
1. Contact a member of the TransportationCamp team to get access to the repository--they'll need your GitHub username.
2. Log in to GitHub, then navigate to [the `transportationcamp.org` repository](https://github.com/openplans/transportationcamp.org).
3. Find the file you want to edit (see _What can I edit?_, below), click on its name, then click on the pencil icon to edit it in your Web browser.
  ![](kZ4HJns7mj.gif)
4. Make your edits, then click the "Commit changes" button at the bottom of the page.

What can I edit?
----------------
There are three main components to the `transportationcamp.org` Web site:
* Camp listings: the banners advertising TransportationCamp events that appear at the top of transportationcamp.org (for upcoming Camps) and at the bottom (for past camps). These are configured in the file `_data/events.yml`.
* Camp pages: Every TransportationCamp event gets its own page, which is linked from the camp listing.  This is visible at `transportationcamp.org/<name of camp>`, and exists in the file `events/<name of camp>/index.md`, where the name of the camp is something like `nyc-2015` or `midwest-2016`.  Camps can also create additional pages for their event in their event's directory.
* Blog posts: TransportationCamp organizers can also create blog posts on `transportationcamp.org` to share news about their event. These are displayed on the homepage, under _What's Happening?_, and at transportationcamp.org/news. Each blog post is a file in the `_posts` directory, like `_posts/2016-02-02-voices-from-2016.md`.

### Creating a camp listing
Edit the file `_data/events.yml`.  At the bottom of the file, add a blank line, then paste in the template below, and modify it with your Camp's details.

```
- title: Texas 2016
  date: 2016-06-26 23:59:59
  url: /events/texas-2016
  register_url: http://www.asce-ictd.org/transportationcamp/
  background_img: houston-2016.jpg
```

What do you need to change?
The `title` line should reflect the name of your Camp; usually a location and a year.
The `date` line is used to display the date of the event in the listing, and also specifies when the Camp listing will move from the top of the homepage (the "Upcoming" section) to the bottom (the "Past Events" section.  You should be able to leave the time set to midnight, and just change the date to the day of your event.
`url` and `register_url` specify the links for more information about the camp and for participants to register.  If your Camp isn't yet open for registration, just omit the `register_url` line.  If your Camp's information page is hosted at `transportationcamp.org` (as is usually the case), then the `url` will be set to `/events/<name of camp>`.
Finally, `background_img` sets the background image which is used for the Camp listing--this should be the name of a file which has been uploaded to `assets/images`.

Note that this is a YAML file, so the indentation of lines is important--the first line is prefixed by a hyphen and a space, while the following lines are prefixed by two spaces. (If you copy and paste this example, you'll already have the right indentation!)


Languages you might need to know
--------------------------------

* Markdown
* HTML (and CSS)
* YAML

Previewing changes to `transportationcamp.org` on your computer
---------------------------------------------------------------


