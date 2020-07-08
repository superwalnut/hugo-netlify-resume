# hugo-blog-netlify-resume
This is a example of using Hugo blog to create a resume site on netlify

# Installing Hugo


## MacOS
brew install hugo

## Windows
choco install hugo -confirm

https://gohugo.io/getting-started/installing/

# check hugo version
hugo version

# create a blog
hugo new site hugo-netlify-resume

# add a theme
git clone git@github.com:aerohub/hugo-orbit-theme.git

cp -R --exclude .git hugo-orbit-theme hugo-netlify-resume/themes/ 

cd sample-resume

# config
copy the themes/orbit/exampleSite/config.toml to the root folder or replace content with it.

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


# netlify

you can get one free site published in netlify with free plan.

Sites -> New site from git -> Select GitHub (for this case) -> Authorize netlify api for access your repository -> select the repository and branch to deploy to netlify