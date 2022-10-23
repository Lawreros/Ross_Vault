## Personal Website
This is where I'll keep instructions/notes on the steps I've taken when building my website, as well as the changes that I have made over time:

### Running Locally

- Took a bit to get the website working for building locally. Turns out that the ubuntu update I had resulted in my `ruby2.7` version disappearing... 
	- Okay, this was a whole series of commands that needed to occur:
	- install and update `bundler` (may not have done anything): https://stackoverflow.com/questions/64867127/how-to-repair-jekyll-and-bundle-installation
	- Install the `github-pages` gem from here: https://kbroman.org/simple_site/pages/local_test.html
	- Then include `webrick` https://stackoverflow.com/questions/69890412/bundler-failed-to-load-command-jekyll
- Yeesh, with all that, now all I need to run is `bundle exec jekyll serve --livereload` where you can do `--livereload` if you are feeling spicy


### Design Ethos
The purpose of this website is two-fold:
1. Advertise the work that I've done
2. Keep me thinking about how to present my work to others (documentation, user experience, etc.)
With that in mind the format and design for each tab/page is pretty simple:
- `About Me`: A quick summary of who I am and  what I am interested in
- `CV`: A copy of my resume/cv for easy download by others
- `Publications`: Links and summaries for my different publications
- `Talks`: Links to any posters/videos that I made for my work
- `Blog Posts`: Monthly updates on the work that I've been doing. This also serves as a hook to keep me coming back and making changes to my website.

### Major Changes
All major changes will to formatting will have the `//Note:` comment put next to them with a description as to what this addition/change does.


### Important File Locations
Which files in the sea of `.css` and markdown are responsible for different formatting and were specifically in those files to look.

#### Content
`images/custom/`: The location of all images that were not part of the default github pages set. This just prevents me from breaking anything before I get a better understanding of what all the different images are for.

#### Formatting
`_sass/_base.scss`: Contains the variable settings for the base html stuff. This is where the margins are defined for fundamental things like `h2` or `<p>` or `<img>`

`_sass/_variables.scss`: Contains the assignment of colors for the website as well as other formatting variables (i.e. so you only have to change the widths/locations once for it to be reflected across the website)

`_sass/_sidebar.scss`: Contains the settings for the author picture and information displayed in the sidebar on the left of the website

`_sass/_pages.scss`: Contains the formatting for the individual Blog Post and Project description pages.

`_sass/_archive.scss`: Contains the formatting for the Blog Post and Project previews, as well as the About page. Pretty much anything that gets converted from markdown to html uses this formatting stuff.