## Step 1. Configure Pelican
    $ pelican-quickstart
It will ask you many questions to set up your site. I use the following settings, mostly I just use the default, below are the answers I provided to launch this test application. You can refer to mine if you are stuck anywhere. The questions are largely straight-forward.

    > Where do you want to create your new web site? [.]
    > What will be the title of this web site? Buttermilch
    > Who will be the author of this web site? Tony Stark
    > What will be the default language of this web site? [en]
    > Do you want to specify a URL prefix? e.g., http://example.com   (Y/n) n
    > Do you want to enable article pagination? (Y/n)
    > How many articles per page do you want? [10]
    > Do you want to generate a Fabfile/Makefile ... and publishing? (Y/n)
    > Do you want an auto-reload & simpleHTTP ... and site development? (Y/n)
    > Do you want to upload your website using FTP? (y/N)
    > Do you want to upload your website using SSH? (y/N)
    > Do you want to upload your website using Dropbox? (y/N)
    > Do you want to upload your website using S3? (y/N)
    > Do you want to upload your website using Rackspace Cloud Files? (y/N)
    > Do you want to uplad your website using Github Pages? (y/N) y
# Step 2. Create a Markdown Post

Your path will be populated with many files now. What you will need is just to create a Post, so that you will see your post later. Navigate to content and create a test.md file. The .md is the file type extension for a markdown file. The Markdown syntax can be found at [Daring Fireball](https://daringfireball.net/projects/markdown/syntax "MarkDown Syntax"). Markdown syntax is suppose to enlighten the work of writing an article and let the writer to focus mainly on the content, that being said, the syntax for formatting used in Markdown is really simple.    

Begin every post.md with the following meta-data.

    Title: Post_Title
    Date: 2013-08-22 16:08
    Category: Post_Category
    Tags: comma, separated, tags
    Summary: This will be used for rss feed generation(and other stuff?).

    ## This is an Eye Catching Heading
    This is the body of my post.


## Step 3. Test Your Local Site
    make devserver
    make html
    make serve

Now point your web browser to [localhost:8000](http://localhost:8000 "Your site should be here").    

f you’d prefer to have Pelican automatically regenerate your site every time a change is detected (handy when testing locally), use the following command instead:

    $ make regenerate

## Step 4. Commit Your Changes

    $ git add .
    $ git commit -m "first commit"
## Step 5. Create a gh-pages Branch and Run the ghp-import script
    $ git branch gh-pages
    $ ghp-import output
    $ git checkout master
    $ git merge gh-pages
    $ git push --all
Your Github Pages site should be live soon.

## Future Posts

The next time you write a post repeat the following steps:

    make html
    git branch gh-pages
    ghp-import output
    git checkout master
    git merge gh-pages
    git push --all
