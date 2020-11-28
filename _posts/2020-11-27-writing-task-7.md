---
layout: post
title:  "Building this website"
date:   2020-11-27 14:00:00 -0600
categories: blog-post writing-task
image: /assets/images/writing-task-7-pic.png
---

Through this article I will be going over the process I took to create this website,  first up, how do I get online?

## Picking a service
First task, I had to pick how I was to create and host my website. I had some options:
* [Google Sites](https://sites.google.com/)
* [Wix](https://www.wix.com/)
* [Squarespace](https://www.squarespace.com/)
* [Wordpress](https://wordpress.com/)
* [GitHub Pages](https://pages.github.com/)

So down the list, discarding as I went until I landed on GitHub Pages. It could be as flexible as I needed it to be, and I already had an account set up. With my service picked out it was time to get to work.

## Experimentation
After experimenting with my own code for a while I decided to switch gears and use a [static site generator](https://www.netlify.com/blog/2020/04/14/what-is-a-static-site-generator-and-3-ways-to-find-the-best-one/) known as [Jekyll](https://jekyllrb.com/). By using Jekyll I could focus on the content of my website rather than just getting my website to work. I can do that because Jekyll allows me to write my content up in [markdown](https://daringfireball.net/projects/markdown/syntax), which is faster to write than HTML. Jekyll then applies a template to the markdown files to create the HTML pages, which it then uses to serve the website. So I got to installing Jekyll.

## Setting things up
With Jekyll now installed, I got to work setting up my website locally, which really boiled down to opening the folder I wanted to store my website in with Git Bash and using the following command: 

```
jekyll new website-name
```

Then I open up my new folder in Git Bash and run the following command. 

```
bundle exec jekyll serve --watch
```

Then by checking https://localhost:4000 I can see my website. At this point it has no personalized content, but it's working so it's time to customize.

## Customizing my website
Before anything else I need a better-looking theme for my website. After some digging I found [Basically Basic](https://github.com/mmistakes/jekyll-theme-basically-basic), which is clean, simple, has good documentation, and it has a few nice extras built-in. I download the files I needed off of their git repository and added them to my website folder.

Next up I worked through the configuration files setting all the values to what I wanted. I then did some testing and bug fixing. Continuing on, I started adding my content to my website, filling out my webpages and adding posts. First I converted them to markdown and added the header details for Jekyll. Then I created an assets folder in my root so that I can add in my images. After a quick check everything appeared to be working.

## Launching the site
To start, I first create a git repository that is named in the following structure username.github.io, this specific repository name allows me to use GitHub Pages. Then using the GitHub Desktop app, I add the repository and copy all my files in. Now before it will work I had to do three things:

1. Switch the `gem jekyll` to `gem "github-pages", group: :jekyll_plugins` in my Gemfile.
2. Switch `theme: jekyll-theme-basically-basic` to `remote_theme: "mmistakes/jekyll-theme-basically-basic"` in my _config file.
3. then run the `bundle update` command using Git Bash in the repository.

Then *voilà* my website has launched. After polishing it up a bit more I have what is now before you.

## Conclusion
That is the overview of my process from start to finish. Beginning with selecting a web service, followed up by some experimentation that led me to use Jekyll. Next was setting the website up, then it was customizing it and adding content. Before ending with launching the site through GitHub Pages.

> *Splash Image by [200 Degrees](https://pixabay.com/users/200degrees-2051452/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1653351) from [Pixabay](https://pixabay.com/?utm_source=link-attribution&amp;utm_medium=referral&amp;utm_campaign=image&amp;utm_content=1653351)*
