---
Type: articles
tags:
  - Readwise
Author: thunderbong
URL: https://engineercodex.substack.com/p/how-instagram-scaled-to-14-million
Summary: Article URL https://engineercodex.substack.com/p/how-instagram-scaled-to-14-million
Comments URL: https://news.ycombinator.com/item?id=37532355
Points: 252
Related: 
Processed: false
owner: Tanzeel159
repo: Digital-Garden-Content
attachment: true
dataview: false
share: true
date created: 2024-10-20 08:11:35
date modified: 2024-10-20 11:08:31
---
![rw-book-cover](https://news.ycombinator.com/favicon.ico)

## Highlights
- Instagram scaled from **0 to 14 million users in just over a year**, from October 2010 to December 2011. They did this with only **3 engineers.** ([View Highlight](https://read.readwise.io/read/01hajx14xyx9scf5m0g3925w9d))
- Instagram’s Guiding Principles ([View Highlight](https://read.readwise.io/read/01hajx1h3c1p19pjjytnj3qg9p))
- Keep things very simple. ([View Highlight](https://read.readwise.io/read/01hajx1kentppjwz1s1rvg9609))
- Don’t re-invent the wheel. ([View Highlight](https://read.readwise.io/read/01hajx1mkdz955hdtmffgde2v8))
- Use proven, solid technologies when possible. ([View Highlight](https://read.readwise.io/read/01hajx1pebjhwjtkkq8ftc2zv9))
- Session: A user opens the Instagram app. ([View Highlight](https://read.readwise.io/read/01hajx34h4jgyt1xnrnbs8e5bv))
- ![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fb1f72ce0-1963-4176-a493-517a1788a277_374x395.png) ([View Highlight](https://read.readwise.io/read/01hajx44z2mxz507f0jsvkr29g))
- Session: After opening the app, a request to grab the main feed photos is sent to the backend, where it hits Instagram’s load balancer. ([View Highlight](https://read.readwise.io/read/01hajx383vyhd9s4nha0d5dwz4))
- ![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fc2e2b88d-751d-4c2c-b87e-95cd90aef20e_642x395.png) ([View Highlight](https://read.readwise.io/read/01hajx47p7zxz7k8wpsqcqvh2e))
- Session: The load balancer sends the request to the application server, which holds the logic to process the request correctly. ([View Highlight](https://read.readwise.io/read/01hajx4d04s6kx1xh1af50ywdc))
- Instagram’s application server used **Django** and it was written in Python, with **Gunicorn** as their WSGI server. ([View Highlight](https://read.readwise.io/read/01hajx4y99j8s7j3msrsykkw67))
- As a refresher, a WSGI (Web Server Gateway Interface) forwards requests from a web server to a web application. ([View Highlight](https://read.readwise.io/read/01hajx4z25nep1x4410watj2p2))
- ![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fd644ba96-4f13-4fe2-8e9f-e01cdec85171_1005x395.png) ([View Highlight](https://read.readwise.io/read/01hajx5gksh3qez7xhdehdywp8))
- Session: The application server sees that the request needs data for the main feed. For this, let’s say it needs: ([View Highlight](https://read.readwise.io/read/01hajx5mv853tgh1g4t45veqgb))
- latest relevant photo IDs ([View Highlight](https://read.readwise.io/read/01hajx5xt3hy1yv5qhkfe90pa1))
- the actual photos that match those photo IDs ([View Highlight](https://read.readwise.io/read/01hajx5yk37sa8gqjjxd6qtrfw))
- user data for those photos. ([View Highlight](https://read.readwise.io/read/01hajx5zakpmvq47axc97ebmp2))
- Session: The application server grabs the latest relevant photo IDs from Postgres. ([View Highlight](https://read.readwise.io/read/01hajx61acxcempbb7mf4aramf))
- **An interesting challenge that Instagram faced and solved is generating IDs that could be sorted by time.** Their resulting sortable-by-time IDs looked like this: ([View Highlight](https://read.readwise.io/read/01hajx8pzqw90sad7yy3650jcd))
- 41 bits for time in milliseconds (gives us 41 years of IDs with a custom epoch) ([View Highlight](https://read.readwise.io/read/01hajx8ttyknm21n5x0299f3kd))
- 13 bits that represent the logical shard ID ([View Highlight](https://read.readwise.io/read/01hajx8vp0g3rf5q18e9y3frg7))
- 10 bits that represent an auto-incrementing sequence, modulus 1024. This means we can generate 1024 IDs, per shard, per millisecond ([View Highlight](https://read.readwise.io/read/01hajx8yxrkawmxdntfab5qyvt))
- Thanks to the sortable-by-time IDs in Postgres, the application server has successfully received the latest relevant photo IDs. ([View Highlight](https://read.readwise.io/read/01hajx91qkyz3rpy9k0z1wzsnk))
- Session: To get the user data from Postgres, the application server (Django) matches photo IDs to user IDs using Redis. ([View Highlight](https://read.readwise.io/read/01hajxb5361hknveekn04e3fzx))
- Instagram used **[Redis](https://instagram-engineering.com/storing-hundreds-of-millions-of-simple-key-value-pairs-in-redis-1091ae80f74c)** to store a mapping of about 300 million photos to the user ID that created them, in order to know which shard to query when getting photos for the main feed, activity feed, ([View Highlight](https://read.readwise.io/read/01hajxbjh577t4zqa4wye0ptwz))
- For general caching, Instagram used **Memcached**. They had 6 Memcached instances at the time. Memcached is relatively simple to layer over Django. ([View Highlight](https://read.readwise.io/read/01hajxct1gvwbn74r1fz9pzd3q))
- Session: The user now sees the home feed, populated with the latest pictures from people he is following. ([View Highlight](https://read.readwise.io/read/01hajxcwp1kxg8dedg1vv6v9hg))
- ![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2F96c6476f-b900-4591-a672-295048bda0a4_1466x597.png) ([View Highlight](https://read.readwise.io/read/01hajxcywwc499kdb3fm5er2rt))
- Session: Now, let’s say the user closes the app, but then gets a push notification that a friend posted a photo. ([View Highlight](https://read.readwise.io/read/01hajxdqexgexr22pm94ywp63c))
- **This push notification was sent using [pyapns](https://github.com/samuraisam/pyapns)**, ([View Highlight](https://read.readwise.io/read/01hajxeccwwabdeza6fakgq6vn))
- Pyapns is an open-source, universal Apple Push Notification Service (APNS) provider. ([View Highlight](https://read.readwise.io/read/01hajxeg75jykehan390dpc4g4))
- Session: The user really liked this photo! So he decided to share it on Twitter. ([View Highlight](https://read.readwise.io/read/01hajxerrtfchcgvpdt2mzh2pm))
- Session: Uh oh! The Instagram app crashed because something erred on the server and sent an erroneous response. The three Instagram engineers get alerted instantly. ([View Highlight](https://read.readwise.io/read/01hajxfxv6x16tmj7aa1dx04z1))
- Final Architecture Overview ([View Highlight](https://read.readwise.io/read/01hajxgfhg560z9xyjz0np8br8))
- ![](https://substackcdn.com/image/fetch/w_1456,c_limit,f_auto,q_auto:good,fl_progressive:steep/https%3A%2F%2Fsubstack-post-media.s3.amazonaws.com%2Fpublic%2Fimages%2Fa279781f-8c76-4e67-8a63-6b9930d1a48c_1984x937.png) ([View Highlight](https://read.readwise.io/read/01hajxgg57pvvtygexe590kafj))
