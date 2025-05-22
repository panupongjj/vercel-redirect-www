{
  "redirects": [
    {
      "source": "/(.*)",
      "destination": "https://jay-downunder.dev/$1",
      "permanent": true
    }
  ]
}

/(.*) means: match everything after the / in the URL.

Example: https://www.jay-downunder.dev/about → matches about

Example: https://www.jay-downunder.dev/blog/post → matches blog/post

$1 is the value matched by (.*)

So if a user visits https://www.jay-downunder.dev/about, it redirects to:
https://jay-downunder.dev/about


################################################################################
If you don’t want to preserve the path, and always redirect to just the homepage, then use this instead:
***** REMOVE $1 *******


{
  "redirects": [
    {
      "source": "/(.*)",
      "destination": "https://jay-downunder.dev",
      "permanent": true
    }
  ]
}
