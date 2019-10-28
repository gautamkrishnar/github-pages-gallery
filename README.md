# Github Pages Gallery
Host your photo/video gallery in Github pages easily using Thumbsup & Travis CI for free.

### Why this project?
This project contains starter code for anyone who wants to deploy his/her photo/video galery on Github Pages, 
**Zero Coding Needed**. Since Github pages is a free hosting service offered by Github to host static pages, it 
offers a decent bandwidth. So it is a great choice for photographers to showcase their works. Travis-CI is a CI & CD
platform that offers unlimited builds for open source projects. Combining the power of GitHub pages with Travis CI is
a zero dollar solution to get your gallery online.

### How to use
Follow the steps below to get your Gallery online. You will be using GitHub web interface to do everything. 
:wink: No frustrating CLIs:
1. SignUp for a Github account and verify your email ID: https://github.com/join
2. Fork this repository:
![fork](https://user-images.githubusercontent.com/8397274/47970004-a0fd9880-e0a5-11e8-8f46-966e21d39c87.gif)
3. Edit [config.json](config.json) by clicking on the edit button (forked repo):

```
{
  "input": "./gallery",
  "output": "./build_output",
  "title": "Photo Gallery", // Set your gallery title here
  "sort-albums-by": "title",
  "sort-media-by": "filename",
  "download-photos": "copy",
  "cleanup": true,
  "theme": "cards", // Your theme
  "theme-style": "./custom.css",
  "footer": "Copyright Text", // Set your copyright text here
  "usage-stats": false
}
```
You can chose from any of the theme below to set the value for theme key:
* `mosaic` - https://thumbsup.github.io/demos/themes/mosaic/
* `cards` - https://thumbsup.github.io/demos/themes/cards/
* `classic` - https://thumbsup.github.io/demos/themes/classic/ 

You can learn more about the configuration file here: https://thumbsup.github.io/docs/3-configuration/usage/. Click on the commit changes button below the page.

4. Create a new account at https://travis-ci.org. Grand all access permission to Github account while signing up.
5. After signing in enable the repo by toggling the switch:
![travis](https://user-images.githubusercontent.com/8397274/47970260-33ec0200-e0a9-11e8-99e0-c94fe41034cf.gif)
6. Go to the project's page by clicking on the project name:
![project](https://user-images.githubusercontent.com/8397274/47970299-8e855e00-e0a9-11e8-9218-64cf97402776.png)
7. Click on More options menu > Settings:
![settings](https://user-images.githubusercontent.com/8397274/47970319-da380780-e0a9-11e8-837a-4a734cceba7a.png)
8. Scroll down to "Environment Variables" section. Add a new environment variable named **GITHUB_TOKEN**:
![token](https://user-images.githubusercontent.com/8397274/47970352-43b81600-e0aa-11e8-93bc-8590208b74a7.png)
9. To set the value of the token, open a new tab and create a token from Github by visiting: https://github.com/settings/tokens.
10. Click on **Generate New Token** button. Type any name you like. Make sure that you had selected all repo permissions given below 
for the token: 
![authtoken](https://user-images.githubusercontent.com/8397274/47970413-f5efdd80-e0aa-11e8-96b0-50199855b9b3.png)
11. Scroll down and click on the Generate token button. Copy the token you see on the page:
12. Paste the token into the environment variable's value input box in Travis CI:
![toekenenv](https://user-images.githubusercontent.com/8397274/47970465-b1b10d00-e0ab-11e8-8873-abf122708773.png)
13. Click on the Add button. Now you are all set.

#### Adding a new album to gallery
1. Go to the gallery folder of the forked repo.
2. Click on Create a new file button.
3. Type AlbumName/.gitkeep in the input box
4. Click Commit Changes button at the bottom.

![newfolder](https://media.giphy.com/media/455paOHOAWr4KWNOtg/giphy.gif)

#### Adding Medias
1. Go to gallery folder. Open any albums if any.
2. Click on Upload files button
3. Select files. Once it finishes upload, click Commit Changes button.

![selectmedia](https://media.giphy.com/media/2uIfenjYx5anbQOEAo/giphy.gif)

#### Find your website URL
If you had done all the above steps then your website will be live now. Please check travis CI for the sttaus of the 
deployment. You can see a build passing badge like the one below:

![travis](https://user-images.githubusercontent.com/8397274/48001817-a99ab100-e12f-11e8-915a-f7a787eb6b0b.png)

#### Select gh-pages branch as the source for Github pages
Now visit your forked repo on GitHub. Click on the settings tab. Scroll down to GitHub pages. Make sure that you have the **gh-pages** brach selected as the **Source** for the GitHub pages. 

Now you can see the URL of the site:
![url](https://user-images.githubusercontent.com/8397274/48008065-f639b880-e13e-11e8-9f8e-72d27ad7cc30.png)

Rename the repo if you need something like `/gallery'. You can even set a custom domain to your site: https://help.github.com/articles/adding-or-removing-a-custom-domain-for-your-github-pages-site/

## Limitations
* Github Pages [terms of service](https://help.github.com/articles/github-terms-of-service/):
> If your bandwidth usage significantly exceeds the average bandwidth usage (as determined solely by GitHub) of other GitHub customers, we reserve the right to immediately disable your account or throttle your file hosting until you can reduce your bandwidth consumption.

This is too unlikely to happen. You can easily setup [Netlify](https://www.netlify.com/) on gh-pages branch to host your site, if you need unlimited bandwidth. 

* File size limit (100 MB) & Repo size limit (75 GB) & Upload limit(25MB): Github limits the maximum usable firesize as 100MB for all files. This is enough for most users. It also imposes a repo size limit of 75GB. If you add a file to a repository via a browser, the file can be no larger than 25 MB. Visit https://help.github.com/articles/what-is-my-disk-quota/ for more info.


## Tools Used
* [Travis CI](https://travis-ci.org/) For continuous deployment.
* [Thumbsup](https://thumbsup.github.io/) for gallery static page generation.
* [GithHub Pages]() for hosting.

## Contributing
Feel free to make any changes and submit a PR.
