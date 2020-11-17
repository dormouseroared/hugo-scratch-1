---
title:  "hugo site on the home network"
date:  "2020-07-02"
author:  "boogy"
authorTwitter:  "" #do not include @
cover:  "hugo cant be reached.png"
tags:  ["hugo", "home network"]
description:  "lots to learn here"
showFullContent:  false
---
# Getting the hugo terminal site visible on the home network

From RED, tried to access the running *hugo server* with ""http://192.168.1.137:1313 but got "this site can't be reached". Tried disabling Linux Mint firewall (no firewall on RED). 

With no change, decided to do a "hugo" to build the pages and use another web server to supply them.

Once the pages are built, they can be copied to the apache2 folder. Note that this does not clear the folder out first.
```
sudo cp -r * /var/www/html/
```


```
                   | EN  
-------------------+-----
  Pages            | 36  
  Paginator pages  |  0  
  Non-page files   |  0  
  Static files     | 16  
  Processed images |  0  
  Aliases          | 12  
  Sitemaps         |  1  
  Cleaned          |  0  
```

# python web server

Navigate to the public folder, then:

```
python -m SimpleHTTPServer 8000
```
No module named SimpleHTTPServer

```
python -m http.server 8000
```

This supplied the site pages but without any format, colours, etc so just blue text on a white background.

# apache2 web server

Installed this on Linux Mint 19.3, then "localhost" without any port, so defaulting to port 80, showed the default apache2 web page. 

# View Page Source

Decided to have a look at the html to spot the difference between the localhost:1313 and the web server version. Straight away saw that example.com was all over the css references. 

There's a parameter in config.toml:

```
baseURL:  "http://www.example.com/"
that needs to be changed to the destination of the web pages
baseURL:  "http://192.168.1.137"
```

##Summary

* hugo server can't be accessed from other computers in the home network, but if "hugo" is run, the generated web pages can be served by apache2, python, or nginx (not yet tried).

* You can use multiple configuration files for direct hugo server (on your own computer), development (on your local network apache) or production (on your hosted service). Have a look at this doc: https://gohugo.io/getting-started/configuration/

* There is perhaps a better solution, just for you: use only relative URLs.

>As your website is on your Apache’s root, you can use | relURL filter instead of | absURL filter in your theme. And add a relativeURLs : true in your configuration file. You have to modify the theme. So you can use exactly the same website with your local hugo server, your Apache and the production website (if the production website is on the root).
