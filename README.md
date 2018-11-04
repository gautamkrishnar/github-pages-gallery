# Github Pages Gallery
Host your photo/video gallery in GitHub using Github pages easily using Thumbsup & Travis CI for free.

### Why this project?
This project contains starter code for anyone who wants to deploy his/her photo/video galery on Github Pages, 
**Zero Coding Needed**. Since Github pages is a free hosting service offered by Github to host static pages, since it 
offers unlimited bandwidth it is a great choice for photographers to showcase their works. Travis-CI is a CI & CD
platform that offers unlimited builds for open source projects. Combining the power of GitHub pages with Travis CI is
a zero dollar solution to get your gallery online.

### How to use
Follow the steps below to get your Gallery online. You will be using GitHub web interface to do everything. 
:wink: No frustrating CLIs:
1. SignUp for a Github account and verify your email ID: https://github.com/join
2. Cone this repository:
![Clone](https://user-images.githubusercontent.com/8397274/47970004-a0fd9880-e0a5-11e8-8f46-966e21d39c87.gif)
3. Edit [config.json](config.json) by clicking on the edit button (forked repo):

```json
{
  "input": "./gallery",
  "output": "./build_output",
  "title": "Photo Gallery", // Set your gallery title here
  "sort-albums-by": "title",
  "sort-media-by": "filename",
  "download-photos": "copy",
  "cleanup": true,
  "theme": "cards",
  "theme-style": "./custom.css",
  "footer": "Copyright Text", // Set your copyright text here
  "usage-stats": false
}
```
Uses of other keys will be explained later. Click on the commit changes button below the page.

4. Create a new account at https://travis-ci.org. Grand all access permission to Github account while signing up.
5. After signing in enable the repo bby troggling the switch:
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
1. Go to the [gallery](gallery) folder of the cloned repo.
2. Click on Create a new file button.
3. Type AlbumName/.gitkeep in the input box
4. Click Commit Changes button at the bottom.

![newfolder](https://media.giphy.com/media/455paOHOAWr4KWNOtg/giphy.gif)

#### Adding Media
1. Go to [gallery](gallery) folder. Open any albums if any.
2. Click on Upload files button
3. Select files. Once it finishes upload, click Commit Changes button.
