# video.js v7.2.1 blob url issue reproduction

this repo offers a simple reproduction case for an issue with blob url compatibility
which was introduced with video.js v7.2.1

## usage

clone repo, spin up a little webserver (eg `python -m SimpleHTTPServer`) and check
`index-7.2.0.html` (works) and `index-7.2.1.html` (doesn't work).

what happens is that videojs never sets its source cache correctly when a blob url is being passed as src and therefor it thinks that the sources are not ready (or sth like that...)

this was introduced with this PR: https://github.com/videojs/video.js/pull/5371
