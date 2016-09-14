+++
comments = false
date = "2016-09-14T16:37:18+01:00"
#draft = true
slug = ""
title = "Building my website - Version II"
toc = false

+++

# What?!

...I got everything working, but then I was thinking to myself why do I need to have such a heavy stack just for creating a few pages ?!

Also I've found out that github pages supports custom domains...**yeah - free hosting!**


## So...
I will go with the following stack:

1. [Github pages](https://pages.github.com/)

2. [Hugo](https://gohugo.io/) - static page generator

3. [Vec](https://github.com/IvanChou/yii.im) - for my hugo theme

4. [Cloudflare](https://cloudflare.com)

I had to create two git repo's:

1. A repo for my source files for hugo (https://github.com/erankeren/erankeren.com-site)

2. A repo for serving my github page (https://github.com/erankeren/erankeren.github.io)

Now I had to change the dns records in cloudflare to point to my github page. 

# Oops...
It was working fine with just one glich: Github pages doesnt support SSL with custom domain (**really...why??**)

## Finally

I could have just use HTTP but my security background didn't allow me to do so.

And then I've found this post in the cloudflare blog:
https://blog.cloudflare.com/secure-and-fast-github-pages-with-cloudflare/

***...Yeah... :-)***





