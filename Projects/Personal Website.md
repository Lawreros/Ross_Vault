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
Where to put the rationale behind the organization of the website.


### Major Changes

### Important File Locations
Which files in the sea of `.css` are responsible for different formatting and were specifically in those files to look.