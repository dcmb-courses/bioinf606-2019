# bioinf606-2019
## Biocomputing bootcamp website for 2019

See: http://dcmb-courses.github.io/bioinf606-2019/

**Overview:** This is a simple [jekell based static site](http://jekyllrb.com/docs/home/). To view locally on your own machine (i.e. before pushing or submitting a pull 
request to this [bioboot GitHub](https://github.com/bioboot/web-2017) repo) 
you will need to have the **jekyll** and **github-pages** gem setup (see further 
below for full instructions)


### Roll forward instructions...

**update 2019** used git mirror to clone 2018 site

To roll forward for a new years class follow the steps below (assuming you already have **jekyll** and **github-pages** 
setup on your local machine):

Git clone old site to a new dir

  	cd ~/Dropbox/Teaching
  	mkdir Bootcamp_2017
  	cd Bootcamp_2017
  	git clone git@github.com:bioboot/web-2016.git web-2017
  	cd web-2017/
  
Update `_config.yml` and `index.md`. IN particular, rembember to change the dates and the pre-course questionnaire and post-course evaluation forms. Go through the regular `git add`, `git commit -m` cycle. But don’t yet push to GitHub (as we will want a new repo for this years class).
  

On GitHub make a new repo (Use the “+” sign and name it `web-2017` to match your local directory name. This name matching is purely for convenience).

Then on the local machine change your remotes to point to this new repo.

  	git remotes -v   
  	git remote rm origin  

Now add our new repo and push changes:  

  	git remote add origin git@github.com:bioboot/web-2017.git  
  	git push -u origin gh-pages  

Then preview your new site online: https://bioboot.github.io/web-2017/ and visit the repo itself to see if everything is ship-shape: https://github.com/bioboot/web-2017  


### Biocomputing bootcamp website for 2016 

See: http://bioboot.github.io/web-2016/  asnd 2015 site setup details below.


### Biocomputing bootcamp website for 2015, 

See: http://bioboot.github.io/web-2015/ This is a simple [jekell based static site](http://jekyllrb.com/docs/home/). 

To view locally on your own machine (i.e. before pushing or submitting a pull 
request to this [bioboot GitHub](https://github.com/bioboot/web-2015) repo) 
you will need to have the **jekyll** and **github-pages** gem setup, i.e.:

Consider updating RubyGems first (likely need sudo for these).

	sudo gem update --system

Then install the Jekyll Gem and the GitHub Gem

	gem install jekyll
	gem install github-pages

Optional: Pygments python based syntax highlighter

	pip install Pygments


## Basics of Jekyll websites
Jekyll websites are configured based on the contents of the various underscore prefixed files and folders. You can find out more about these here: http://jekyllrb.com/docs/structure/

However, most likely you will want to leave most of these alone and just add  
content to the day{2,3,4,5}.md files and create new files in the **class-material/** 
directory (i.e. add lecture slides, handouts, cheat-sheets etc.)

Please remember that all content is on the **gh-pages** branch! 
So you will want to be working on this branch and push back to this branch.

A typical workflow for folks that have been added as **"Collaborators"** would look something like this:

	## One time only clone
	git clone https://github.com/bioboot/web-2015.git
	cd web-2015

	## Edit your files (e.g. day2.md)
	vi day2.md

	## Check changes localy
	jekyll serve

	## Pull recent changes
	git pull origin gh-pages

	## Stage, commit and push your changes
	git status
	git add day2.md
	git commit -m "Your msg about changes"
	git push origin gh-pages


## How this site was built
Basic setup entailed:

	jekyll new 2015
	cd 2015
	## Edited site title, description etc. in _config.yml
	vi _config.yml  
	rm -rf _posts/   ##  we are not going to have a blog
	mv index.html blog.html  ## can delete later

Create a simple index.md file and have a quick look with 'jekyll serve'

	jekyll serve

After some more content addition I then followed the [instructions for adding 
to GitHub pages](http://jekyllrb.com/docs/github-pages/).

#### Cloned from Barry Grant (http://thegrantlab.org/) repository at https://github.com/bioboot/web-2017
