---
layout: post
title:  "Blocking LinkedIn Reactions"
date:   2024-08-15 00:00:01 +0000
categories: general
---
Just thought this might be useful for those already using [uBlock Origin](https://github.com/gorhill/uBlock) .

Add these rules to your My Filters section to block LinkedIn reactions when viewing your feed.

```
linkedin.com##:matches-path(/feed):xpath(//span[text()[contains(.,'likes this')]]/../../../../../../..)
linkedin.com##:matches-path(/feed):xpath(//span[text()[contains(.,'celebrates this')]]/../../../../../../..)
linkedin.com##:matches-path(/feed):xpath(//span[text()[contains(.,'loves this')]]/../../../../../../..)
linkedin.com##:matches-path(/feed):xpath(//span[text()[contains(.,'finds this insightful')]]/../../../../../../..)
linkedin.com##:matches-path(/feed):xpath(//span[text()[contains(.,'finds this funny')]]/../../../../../../..)
linkedin.com##:matches-path(/feed):xpath(//span[text()[contains(.,'supports this')]]/../../../../../../..)
```

Happy blocking!
