+++
comments = false
date = "2016-09-14T16:04:16+01:00"
#draft = true
slug = ""
title = "Building my website - Version I"
toc = false

+++

## Wordpress

At first I thought about building my website using good old wordpress. I thought about the following stack:

1. Amazon ec2 instance for the server

2. Wordpress running inside a docker container (because installing wordpress is a nightmare! and docker is cool...)
	**https://github.com/eugeneware/docker-wordpress-nginx**

3. Nginx - reverse proxy into wordpress inside the docker

4. Cloudflare - for the free ssl certificates and dns manager

I could have just bought a hosted soultion like they offer at **[godaddy](https://uk.godaddy.com/hosting/wordpress-hosting)** but I love playing with stuff.


## Wait...

After installing and configuring all of the above there were two things I had to fix:

1. The theme I was using was pulling google fonts JS using HTTP and not HTTPS, which caused the browser to display an error about mixing HTTP and HTTPS. So i've found this (thanks google):
	http://www.amixa.com/blog/2012/06/06/how-to-use-google-fonts-under-both-ssl-and-non-ssl-without-ssl-insecure-messages/

2. Wordpress is not playing nice behind a reverse proxy, fixed by:
	https://cmanios.wordpress.com/2014/04/12/nginx-https-reverse-proxy-to-wordpress-with-apache-http-and-different-port/
