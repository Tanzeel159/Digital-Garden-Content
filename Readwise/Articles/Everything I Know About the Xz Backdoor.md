---
Type: articles
tags:
  - Readwise
Author: Evan Boehs
URL: https://boehs.org/node/everything-i-know-about-the-xz-backdoor?s=09
Summary: JiaT75's suspicious activity in XZ development raises concerns about potential backdoors and compromised code. The timeline shows a pattern of gaining trust and making changes that could lead to security vulnerabilities. GitHub eventually suspends JiaT75's account.
Related: 
Processed: false
owner: Tanzeel159
repo: Digital-Garden-Content
attachment: true
dataview: false
share: true
date created: 2024-10-20 08:11:36
date modified: 2024-10-20 11:02:37
---
![rw-book-cover](https://boehs.org/og/node/everything-i-know-about-the-xz-backdoor.png)

## Highlights
#### 2021
- The first commits they make are not to xz, but they are deeply suspicious. Specifically, they open a PR in libarchive: [Added error text to warning when untaring with bsdtar](https://github.com/libarchive/libarchive/pull/1609). This commit does a little more than it says. It replaces `safe_fprint` with an unsafe variant, potentially introducing another vulnerability. The code was merged without any discussion, and [lives on to this day](https://github.com/libarchive/libarchive/blob/master/tar/read.c#L374-L375) ([patched](https://github.com/libarchive/libarchive/pull/2101)). libarchive should also be considered compromised until proven otherwise. ([View Highlight](https://read.readwise.io/read/01ht9ex456c9xr8js6gjxwynxf))
#### 2022
- In 2022, pressure to add another maintainer to XZ is [launched](https://www.mail-archive.com/xz-devel@tukaani.org/msg00566.html). ([View Highlight](https://read.readwise.io/read/01ht9exw86w1q6xbcn1qc7tvyw))
- Three days after this email, JiaT75 makes their first commit to xz: [Tests: Created tests for hardware functions.](https://github.com/tukaani-project/xz/commit/aa75c5563a760aea3aa23d997d519e702e82726b). Since this commit, they become a regular contributor to xz (they are currently the second most active). It’s unclear exactly when they became trusted in this repository. ([View Highlight](https://read.readwise.io/read/01ht9ey9jfdy972bj21zag84sj))
#### 2023
- JiaT75 merges their first commit [on Jan 7 2023](https://github.com/tukaani-project/xz/pull/7)[1](https://boehs.org/node/everything-i-know-about-the-xz-backdoor?s=09#fn1), which gives us good indication into when they fully gain trust. ([View Highlight](https://read.readwise.io/read/01ht9ez17p5hpzrb0rrrebmmv7))
- In July, [a PR](https://github.com/google/oss-fuzz/pull/10667) was opened in oss-fuzz to disable ifunc for fuzzing builds, due to issues introduced by the changes above. This appears to be deliberate to mask the malicious changes that will be introduced soon. ([View Highlight](https://read.readwise.io/read/01ht9f0ereesrvhqh6f2xb0yht))
#### 2024
- A pull request for Google’s [oss-fuzz is opened](https://github.com/google/oss-fuzz/pull/11587) that changes the URL for the project from [tukaani.org/xz/](http://tukaani.org/xz/) to [xz.tukaani.org/xz-utils/](http://xz.tukaani.org/xz-utils/). [tukaani.org](http://tukaani.org) is hosted at `5.44.245.25` in Finland, at [this](https://www.zoner.fi/) hosting company. The `xz` subdomain, meanwhile, points to GitHub pages. This furthers the amount of control Jia has over the project. ([View Highlight](https://read.readwise.io/read/01ht9f1jjpy0yjcdqemq78q93d))
#### The discovery
- An email is sent to the oss-security mailing list: [backdoor in upstream xz/liblzma leading to ssh server compromise](https://www.openwall.com/lists/oss-security/2024/03/29/4), announcing this discovery, and doing it’s best to explain the exploit chain. ([View Highlight](https://read.readwise.io/read/01ht9f2bgypxj51xmvnkbfgv7c))
#### A sudden push for inclusion
- A request for the vulnerable version to be included in Debian is opened by Hans: ([View Highlight](https://read.readwise.io/read/01ht9f5yj8kea9ybv5mz568f3q))
