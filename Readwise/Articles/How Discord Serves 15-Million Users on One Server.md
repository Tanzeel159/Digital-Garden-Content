---
Type: articles
tags:
  - Readwise
Author: Dev Notes 🖥️
URL: 
Summary: Discord, the popular communication platform, has expanded the capacity of a single server to support 15 million concurrent users, a significant increase from the previous limit of around 1 million users. This expansion was necessary to accommodate the rapid growth of the MidJourney community. Discord assembled a team of senior engineers to address the scaling challenge, and they made adjustments to technologies like BEAM and Elixir. They also used the programming language Rust to scale Elixir for the massive number of users. Through optimization and creative engineering, the team successfully expanded the guild capacity by 15 times.
Related: 
Processed: false
owner: Tanzeel159
repo: Digital-Garden-Content
attachment: true
dataview: false
share: true
date created: 2024-10-20 08:11:36
date modified: 2024-10-20 11:08:12
---
![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article0.00998d930354.png)

## Highlights
- Discord, the popular communication platform, has achieved a remarkable feat by expanding the capacity of a single server to support 15 million users, a significant leap from the previous limit of around 1 million users. ([View Highlight](https://read.readwise.io/read/01hmgdh4cg0d1dsp0ngpdsxyyh))
- The challenge began when the MidJourney server's growth threatened to surpass Discord's established user limit per server. ([View Highlight](https://read.readwise.io/read/01hmgdh7zhr2yazfpjhcjy3der))
- One of the critical issues encountered was a performance drop due to pathological garbage collection, which occurred when freeing small memory allocations outside the heap. The solution was to tune the virtual binary heap size, which allowed for the enabling of offload and significantly improved throughput. ([View Highlight](https://read.readwise.io/read/01hmgdhgm0dyhfk575587f2hjp))
    - Note: When Discord was serving a lot of people, they noticed that the computer was slowing down when it tried to get rid of small pieces of memory. They fixed this problem by changing how much memory the computer used and it made things faster.
