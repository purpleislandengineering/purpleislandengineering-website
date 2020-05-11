
# Website for Purple Island Engineering

![github pages](https://github.com/purpleislandengineering/purpleislandengineering-website/workflows/github%20pages/badge.svg?branch=master)

## to get the most recent code

(first time) get a local copy

    git clone https://github.com/purpleislandengineering/purpleislandengineering-website.git
    cd purpleislandengineering-website

(subsequent times) get recent changes to the code

    cd purpleislandengineering-website
    git pull https://github.com/purpleislandengineering/purpleislandengineering-website.git

### install hugo-extended

[General instructions](https://gohugo.io/getting-started/installing/)

Mac OSX (extended is default)

    brew install hugo

Ubuntu (snap)

    snap install hugo --channel=extended

Confirm your version is `hugo-extended`

    hugo version

should include the text `extended` after the version number. For example:

    Hugo Static Site Generator v0.70.0/extended darwin/amd64 BuildDate: unknown


## launch the local website

then to build the website
	
	cd purpleislandengeering-website

    hugo

and to serve the website (default port is 1313)

    hugo serve -D

open a browser window to [localhost:1313](http://localhost:1313)


## to deploy to the public web

building the website is done with this [github action](https://github.com/peaceiris/actions-hugo).

commit to the master branch to trigger the build.

The changes should be available on the website after a short (< 1 min) build: http://localhost:1313/purpleislandengineering-website

---

## one-time setup

clone empty repo (created in browser)

    git clone git@github.com:purpleislandengineering/purpleislandengineering-website.git

generate hugo default in that empty repo

    hugo new site purpleislandengineering-website --force

add submodule for [theme](https://github.com/JugglerX/hugo-serif-theme) to [subfolder](https://stackoverflow.com/a/9035930/2327328)

    cd purpleislandengineering-website 
	git clone https://github.com/jugglerx/hugo-serif-theme.git themes/hugo-serif-theme
	#git submodule add https://github.com/JugglerX/hugo-serif-theme.git themes/hugo-serif-theme

add [example content](https://github.com/JugglerX/hugo-serif-theme#add-example-content)

    cp -a themes/hugo-serif-theme/exampleSite/. .

update `config.tom` with this [header text](https://github.com/JugglerX/hugo-serif-theme#update-configtoml)

The page based on the git branch `gh-pages` will be available here: https://purpleislandengineering.github.io/purpleislandengineering-website/