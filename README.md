full article read: https://medium.com/@mrkevin.wang/create-a-web-personal-profile-page-with-hugo-blog-netlify-for-free-9d2b19a83da1

# hugo-blog-netlify-resume
This is a example of using Hugo blog to create a resume site on netlify

# Installing Hugo

## MacOS
brew install hugo

## Windows
choco install hugo -confirm

# installing url
https://gohugo.io/getting-started/installing/

# check hugo version
hugo version

# create a sample blog
hugo new site hugo-netlify-resume

# add a theme and copy it to the sample blog
git clone git@github.com:aerohub/hugo-orbit-theme.git

rsync -r --exclude '.git' hugo-orbit-theme hugo-netlify-resume/themes/ 

# update the example config to our sample blog
copy the themes/orbit/exampleSite/config.toml to the root folder or replace content with it.

# add a test.md in content folder
this is where you can publish blog posts by using markdown formats.

# init git repo and set remote
cd hugo-netlify-resume

git init

git add .

git commit -m "create blog and add theme"

git remote add origin git@github.com:superwalnut/hugo-netlify-resume.git
git push -u origin master

# run hugo locally
hugo server -w

# local url
http://localhost:1313/

# statistics
                   | EN
-------------------+-----
  Pages            |  4
  Paginator pages  |  0
  Non-page files   |  0
  Static files     | 98
  Processed images |  0
  Aliases          |  0
  Sitemaps         |  1
  Cleaned          |  0


# create site in netlify and connect to your github repository.

you can get one free site published in netlify with free plan.

Sites -> New site from git -> Select GitHub (for this case) -> Authorize netlify api for access your repository -> select the repository and branch to deploy to netlify


# add custom domain
you can add a custom domain and apply ssl certificate at netlify as well. It is fairly straight forward.

#  config update site url
set baseurl = "https://modest-newton-b02ee3.netlify.app/" in config.toml


----

# using netlify cli
npm install netlify-cli -g

# login to netlify, this will redirect you to login and Once authorized, Netlify CLI will store your access token in your home folder, under .netlify/config.json. Netlify CLI will use the token in this location automatically for all future commands.
netlify login

# netlify status to view your current user and status
netlify status

# netlify init to connect to your repository and create a site on netlify
netlify init

