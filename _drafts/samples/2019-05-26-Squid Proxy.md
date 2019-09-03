---
layout : "page"
Title : ":/Title"
---
Proxy servers are great. It helps you mask your details and access contents that are geographically restricted. It can also be used as a crucial role in corporation network to ensure people are not surfing through meme during working hours. 

While the later is under controlled environment, you cannot say the same for the free proxy servers that you get online. Logging traffic or in worst case of SSL interception, can be really scary if you connect to sites which requires credentials and if you were to pass through servers. 

With the availability of cloud providers it is easy to launch your proxy servers for personal use. Of course, you would have to pay for running you own services however, it is quite cheap since most are billed on pay as you use/run service.  

Squid Proxy software is a really good software for most of the basic setup and we will learn to built a simple proxy for setup. Squid is available in most repositories. 

Pre-requisites:
---
Public resource to access 

* GitHub Account
It is free for hosting public repository so nothing much to lose.

* Understanding the basic concepts and commands of GitHub
I started off by going through the following Youtube playlist. Simple and cool to learn.

[Git/Github Tutorial](https://www.youtube.com/playlist?list=PLeo1K3hjS3usJuxZZUBdjAcilgfQHkRzW)

* Basic idea on writing HTML websites or working with static site generator such as 'Jekyll' 
I went with Jekyll since it looks to be easier than writing my own HTML code. The following Youtube playlist was awesome to understand a lot of things in a very short time.

[Jekyll - Static Site Generator \| Tutorial](https://www.youtube.com/playlist?list=PLLAZ4kZ9dFpOPV5C5Ay0pHaa0RJFhcmcB)

Steps:
---
1. Create a repository in the format`<github_username>.github.io` :

eg) My GitHub username is 'akhilbaburaj' hence, my repository is 'akhilbaburaj.github.io'
This would be the repository where all you website(s) are hosted. Yes, you can host multiple sites however, the path will be unique if you want to view different sites. Currently, I have no plans to host multiple sites hence, I am hosting the entire site on root repository path(/).

2. Create your HTML pages or copy paste your HTML files(eg. index.html) to your repository folder on you local machine. Since I went with Jekyll, I used it to create a folder named as `<github_username>.github.io` eg. 'akhilbaburaj.github.io'. Jekyll creates a default template of files so it is quite easy to host the template and contents for future articles as well. With help from Jekyll you can test it locally as well before making the commit. 

3. Use GitHub CLI or GitHub Desktop to update your repository:
This should allow you to pull, add, change, commit and then push the files to your repository. 

4. Once the files are pushed, give it some time before trying to load the page on your browser using the URL `http://<github_username>.github.io/` eg.[http://akhilbaburaj.github.io/](http://akhilbaburaj.github.io/). If things are hosted fine then, your still will officially online for public use.

**Note:** You can see that the theme I used does not match the default theme provided by Jekyll. There are tons of Themes available for free and you can use them too however,to test you would have to 'jekyll build' and 'jekyll serve' in the folder when you have your theme. 

If you would like to use custom domain like 'example.io' then, please make to update your DNS records and also the CNAME file. This setting can be configured from your repository's setting section (not. your account/profile section). For more steps please follow the steps mentioned in GitHub's official document:

[Adding or removing a custom domain for your GitHub Pages site](https://help.github.com/articles/adding-or-removing-a-custom-domain-for-your-github-pages-site/)

<br>
<br>

Hope this helps you in directing your path on hosting on GitHub. There are tons of other articles online however, I will recommend that you do go for the most latest article as GitHub has changes quite a bit and some of the earlier steps mentioned are not explicitly required anymore to achieve the same task. 