**Looking for the TransportationCamp website? Go [here](https://transportationcamp.org)!**

`transportationcamp.org` for TransportationCamp organizers
==========================================================
This document is intended to orient TransportationCamp organizers and
The `transportationcamp.org` website is hosted using [GitHub Pages](https://docs.github.com/pages), a service
of [GitHub](https://github.com/). After creating a GitHub account and being
granted access, you can edit pages on `transportationcamp.org` over the Web, without any special tools.

## How to edit `transportationcamp.org`, condensed

0. [Create a GitHub account](https://github.com/join), if you don't already have one.
1. Contact a member of the TransportationCamp team to get access to the repository--they'll need your GitHub username.
2. Log in to GitHub, then navigate
   to [the `transportationcamp.org` repository](https://github.com/openplans/transportationcamp.org).
3. Find the file you want to edit, click on its name, then click the arrow next to the pencil icon and select "Open
   with `github.dev`".
4. This opens the website in an editing environment in your browser. You can edit other files, upload, delete, and move
   files, create folders, etc.
5. When you are done with your edits, click on the `Source Control` icon on the left sidebar (looks like a branch),
   summarize your changes in the `Message` field, then click `Commit and Push`.
6. If all goes well, the website should update in a few minutes with your changes. If the website doesn't update, you
   can see the failed build and what you might need to fix in the `Actions` tab at the top of the repository page.

## Adding a new Camp

### Step 1: Create a Camp page

Every TransportationCamp event gets its own page, which is linked from the homepage. This is visible
at `transportationcamp.org/events/<name of camp>`, and exists in the folder `events/<name of camp>`, where the name of
the camp is something like `nyc-2023`.

It is highly recommended to duplicate an existing camp's folder in `events` to start, and edit the content to fit the
needs of your camp.

The main page for your camp is `index.markdown`, which is written
in [Markdown](https://guides.github.com/features/mastering-markdown/). Most basic formatting is supported directly in
Markdown, but you can also use HTML tags should you desire more customization or need to embed YouTube videos or
registration widgets. To include images, upload them to your event folder, and reference them in the file with an
HTML `<img>` tag
or [Markdown's `!` notation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#images).
Be sure to change the metadata at the top of the page to reflect the name and date of your camp.

You will also need to upload a logo at `logo.png` which will be displayed at the top of the page.

It is highly recommended to optimize all images before uploading them using a service such
as [TinyPNG](https://tinypng.com/).

### Step 2: Upload a banner image

This is the image that appears in large format on `transportationcamp.org`. It will be shown at a variety of aspect
ratios depending on the user's screen size, but the center of the image will always be centered in view. In general,
there is no need for the image to be taller than half its width. Bear this in mind when cropping.

Optimize the image with [TinyPNG](https://tinypng.com/), then upload it to the `assets/event-images` folder. The
filename does not have to match your camp name, but make note of it for Step 3.

### Step 3: Add your Camp to the homepage

Edit the file `_data/events.yml`. At the bottom of the file, add a blank line, then paste in the template below, and
modify it with your Camp's details.

```
- title: PHL
  subtitle: Summer Gathering
  year: 2023
  date: 2023-06-24 23:59:59
  url: /events/phl2023-summer
  register_url: https://tcphl23summer.eventbrite.com/?aff=tcwebsite
  background_img: philly-23-summer-lastyrprizesjpg.jpg
```

What do you need to change?

* `title` should reflect the name of your Camp; usually its location.
* `subtitle` is optional, though you can use it to show ancillary details, such as if you are running a virtual event or
  have more than one event that year
* `year` is the year of your event.
* `date` is the date of your event. Leave the time set to `23:59:59`.
* `url` and `register_url` specify the links for more information about the camp and for participants to register. If
  your Camp isn't yet open for registration, just omit the `register_url` line. If your Camp's information page is
  hosted at `transportationcamp.org` (as is usually the case), then the `url` will be set to `/events/<name of camp>`.
* `background_img` is the filename from Step 2 above.

Note that this is a YAML file, so the indentation of lines is important--the first line is prefixed by a hyphen and a
space, while the following lines are prefixed by two spaces. (If you copy and paste this example, you'll already have
the right indentation!)

### As your event approaches

You can edit your camp page as often as you want. Don't forget to put your registration URL in `_data/events.yml` when
it opens.

When your event concludes, it will remain at the top of the homepage until the site is rebuilt, usually by someone
making an edit. You can force a rebuild by making a trivial edit on your Camp page and saving your changes.

## Previewing changes on your computer

There are five main steps to building the site locally on your computer:

1. [Install Jekyll and Ruby](https://jekyllrb.com/docs/installation/)
2. [Clone the repository to your computer](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
3. The first time you build the website, run `bundle install`
4. Run `bundle exec jekyll serve`
5. If all goes well, you will be able to see `transportationcamp.org` at `http://localhost:4000`.

Learn more
at [GitHub's documentation page](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).
