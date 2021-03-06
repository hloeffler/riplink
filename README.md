# R.I.P.Link

[![Build Status](https://travis-ci.org/mschwager/riplink.svg?branch=master)](https://travis-ci.org/mschwager/riplink)
[![Coverage Status](https://coveralls.io/repos/github/mschwager/riplink/badge.svg?branch=master)](https://coveralls.io/github/mschwager/riplink?branch=master)

![H.R.E.F.](logo.png)

`riplink` finds dead links on the web. It's useful for double-checking web pages for incorrect, or dead web links.

Inspired by Wikimedia and the Internet Archive [fixing broken links on Wikipedia](https://blog.wikimedia.org/2016/10/26/internet-archive-broken-links/), and my curiosity of concurrent programming in Go.

# Installing

```
$ go get github.com/mschwager/riplink
```

# Using

By default `riplink` will only print links to pages that return something other than an `HTTP 200`.

If we specify the `-verbose` flag it will print all links:

```
$ riplink -verbose -url https://google.com
https://www.google.com/intl/en/options/ 200
https://www.google.com/imghp?hl=en&tab=wi 200
https://google.com/intl/en/policies/terms/ 200
https://google.com/intl/en/ads/ 200
https://google.com/services/ 200
...
```

# Testing

```
$ go test ./...
```
